<template>
  <v-container fluid>
    <v-slide-y-transition mode="out-in">
      <v-container no-padding>
        <!-- Title -->
        <v-layout row style="margin-top: 20px">
          <v-flex sm12 xs12 md10 id="comp-title">
            <v-layout class="row">
              <v-flex md12 xs8 style="z-index: 2">
                <h1 class="sherpa-blue heading-large shadow-yellow" align="left">Scoreboard CP</h1>
              </v-flex>
            </v-layout>
          </v-flex>
        </v-layout>
        <v-layout row>
          <v-flex md12 xs8 style="z-index: 2">
            <button
              class="category box-stroke"
              v-bind:class="{ active: cid === 4 }"
              v-on:click="cid = 4, isFetch = true"> Penyisihan Senior </button>
            <button
              class="category box-stroke"
              v-bind:class="{ active: cid === 3 }"
              v-on:click="cid = 3, isFetch = true"> Penyisihan Junior </button>
          </v-flex>
        </v-layout>
        <v-layout row class="dash-size line-fill margin-bottom-sm">
        </v-layout>
        <!-- /Title -->
        <!-- Loading Indicator -->
        <v-flex md12 v-if="this.isFetch == true">
          Please wait...
        </v-flex>
        <!-- Scoreboard -->
        <v-layout margin-bottom-xl class="flex-column overflow-x-auto" v-if="this.scoreboard.length > 0">
          <v-flex md12>
            Last fetch: {{ this.lastFetched }}
          </v-flex>
          <v-flex class="t-row">
            <div class="t-col-rank"> Rank </div>
            <div class="t-col-team"> Team </div>
            <div class="t-col-fill"> </div>
            <div class="t-col-score"> Solved </div>
            <div class="t-col-score"> Time </div>
            <div class="t-col-prob" v-for="problem in this.scoreboard[0].problems" :key="problem.problem_id">
              {{ problem.label }}
            </div>
          </v-flex>
          <v-flex class="t-row" v-for="team in this.scoreboard" :key="team.team_id">
            <div class="t-col-rank"> {{ team.rank }} </div>
            <div class="t-col-team">
              <div class="t-row">
                <div class="t-col-image">
                  <img :src="team.team_image" />
                </div>
                <div class="t-col-team-name">
                  {{ team.team_name }}
                  <br/>
                  <span class="text-small"> {{ team.team_affiliation}} </span>
                </div>
              </div>
            </div>
            <div class="t-col-fill"> </div>
            <div class="t-col-score"> {{ team.score.num_solved }} </div>
            <div class="t-col-score"> {{ team.score.total_time }} </div>
            <div class="t-col-prob" v-bind:class="{ solved: problem.solved, pending: problem.num_pending > 0, judged: problem.num_judged > 0 }" v-for="problem in team.problems" :key="problem.problem_id">
              <div>
                <span v-if="problem.num_judged > 0"> {{ problem.num_judged }} </span>
                <span v-if="problem.num_pending > 0"> + {{ problem.num_pending }} </span>
              </div>
              <div class="text-small" v-if="problem.time"> {{ problem.time }} </div>
            </div>
          </v-flex>
        </v-layout>
        <v-layout v-if="this.lastFetched !== null && this.scoreboard.length === 0" margin-bottom-xl>
          Kontes tidak sedang berjalan.
        </v-layout>
        <v-layout v-if="!this.lastFetched === null" margin-bottom-xl>
          Sedang mengambil data...
        </v-layout>
        <!-- /Scoreboard -->
      </v-container>
    </v-slide-y-transition>
  </v-container>
</template>

<script>
import jquery from 'jquery';

export default {
  name: 'CPScoreboard',
  components: { },
  props: {
    msg: String,
  },
  data: function () {
    return {
      cid: 4,
      scoreboard: [],
      teams: {},
      lastFetched: null,
      isFetch: true,
    };
  },
  watch: {
    cid: async function () {
      this.teams = await this.getTeam();
      this.scoreboard = await this.getScoreboard();
    }
  },
  methods: {
    formatDate: function (date) {
      let hours = date.getHours();
      let minutes = date.getMinutes();
      let seconds = date.getSeconds();
      minutes = minutes < 10 ? '0' + minutes : minutes;
      seconds = seconds < 10 ? '0' + seconds : seconds;
      let strTime = hours + ':' + minutes + ':' + seconds;
      return date.getMonth()+1 + "/" + date.getDate() + "/" + date.getFullYear() + "  " + strTime;
    },
    getTeam: async function () {
      try {
        let url = 'https://cp.arkavidia.id/domjudge/api/teams?cid=' + this.cid;
        let response = await jquery.get(url);
        let result = {};
        for (let i = 0; i < response.length; i++) {
          result[response[i].id] = response[i];
        }
        return result;
      } catch (e) {
        return {};
      }
    },
    getScoreboard: async function () {
      try {
        this.lastFetched = null;
        let url = 'https://cp.arkavidia.id/domjudge/api/scoreboard?cid=' + this.cid;
        this.isFetch = true;
        let response = await jquery.get(url);
        for (let i = 0; i < response.length; i++) {
          response[i].team_name = this.teams[response[i].team_id].name;
          response[i].team_affiliation = this.teams[response[i].team_id].affiliation;
          response[i].team_image = "https://cp.arkavidia.id/domjudge/images/affiliations/" + this.teams[response[i].team_id].team_id + ".png";
        }
        this.lastFetched = this.formatDate(new Date());
        this.isFetch = false;
        return response;
      } catch (e) {
        return [];
      }
    },
    refreshScoreboard: function () {
      let ref = this;
      this.getScoreboard().then((res) => {
        ref.scoreboard = res;
      });
      setTimeout(this.refreshScoreboard, 30000);
    },
  },
  async created() {
    this.teams = await this.getTeam();
    this.refreshScoreboard();
  }
}

</script>

<style scoped>

#comp-title {
  display: flex;
  flex-direction: column;
  justify-content: center;
}

.overflow-x-auto {
  overflow-x: auto;
}

.category {
  padding: 5px 20px;
  margin: 10px 10px 10px 0;
}

.category:not(.active) {
  opacity: .5;
}

.category:first-child {
}

.t-row {
  display: flex;
  flex-direction: row;
}

.t-col-rank, .t-col-team, .t-col-prob, .t-col-score {
  padding: 5px;
  overflow-x: hidden;
}

.t-col-rank {
  flex: 0 0 50px;
  text-align: center;
  display: flex;
  flex-direction: column;
  justify-content: center;
}

.t-col-team {
  flex: 0 0 200px;
}

.t-col-fill {
  flex: 1 1;
}

.t-col-image {
  flex: 0 0 50px;
}

.t-col-score {
  flex: 0 0 75px;
  text-align: center;
  display: flex;
  flex-direction: column;
  justify-content: center;
}

.t-col-prob {
  flex: 0 0 50px;
  text-align: center;
  display: flex;
  flex-direction: column;
  justify-content: center;
}

.t-col-prob.pending {
  background-color: #1cc7e3;
}

.t-col-prob.solved {
  background-color: #10464f;
  color: #fffdf2;
}

.t-col-prob.judged:not(.solved):not(.pending) {
  background-color: #eb4924;
  color: #fffdf2;
}

.text-small {
  font-size: .75em;
}

@media screen and (max-width: 1024px) {
  /* */
}

@media screen and (max-width: 768px) {
  /* */
}

@media screen and (max-width: 480px) {
  /* */
}

</style>

