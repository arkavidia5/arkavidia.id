<template>
  <v-container fluid no-padding>
    <v-layout row section landing>
      <v-responsive :aspect-ratio="18/9" class="primary--text">
        <h1 class="futura-lt bold" style="font-size:3.2vw;position:absolute;bottom: 34.5%; left: 10%;">
          Awakening Future Generation's Potential
        </h1>
        <h1 class="futura-lt bold" style="font-size:4.6vw;bottom:24%;left:10%;position:absolute">
          Through IT
        </h1>
      </v-responsive>
    </v-layout>
    <v-layout row gradient down/>
    <v-layout row section whats-on justify-center>
      <h1 class="futura-lt bold heading">
        What's on Arkavidia?
      </h1>
    </v-layout>
    <v-container>
      <v-layout class="row wrap">
        <v-flex class="md3 xs12 sm6 pa-4">
          <a href="https://itfest.arkavidia.id">
          <div class="bordered">
            <img src="../../assets/dday_itfest.svg" alt="" width="100%">
          </div>
          </a>
        </v-flex>
        <v-flex class="md3 pa-4">
          <router-link to="/competition/cp/scoreboard">
          <div class="bordered">
            <img src="../../assets/dday_cp.svg" alt="" width="100%">
          </div>
          </router-link>
        </v-flex>
        <v-flex class="md3 xs12 sm6 pa-4">
          <a href="http://ctf.arkavidia.id/scoreboard">
          <div class="bordered">
            <img src="../../assets/dday_ctf.svg" alt="" width="100%">
          </div>
          </a>
        </v-flex>
        <v-flex class="md3 xs12 sm6 pa-4">
          <router-link to="/event/arkavtalk#topics">
          <div class="bordered">
          <img src="../../assets/dday_arkavtalk.svg" alt="" width="100%">
          </div>
          </router-link>
        </v-flex>
      </v-layout>
    </v-container>
    <PageBreak/>
    <v-layout row section events justify-center>
       <v-container>
         <v-layout row justify-center>
          <h1 class="futura-lt bold heading">
            Pre-Events
          </h1>
         </v-layout>
        <v-layout row justify-center wrap style="margin-top:15px;">
          <v-flex md2 xs6>
            <router-link to="/preevent/gamejam" class="d-flex justify-center align-center no-decoration black--text flex-column" >
              <img src="../../assets/ggj-01.svg" alt="gamejam-ico" height="150">
              <h3 style="margin-top:4px;">Global Game Jam</h3>
            </router-link>
          </v-flex>
          <v-flex md2 xs6>
            <router-link to="/preevent/codingclass" class="d-flex justify-center align-center no-decoration black--text flex-column"  >
              <img src="../../assets/codingclass-02.svg" alt="codingclass-ico" height="150">
              <h3 style="margin-top:4px;">Coding Class</h3>
            </router-link>
          </v-flex>
          <v-flex md2 xs6>
            <router-link to="/preevent/dataacademy" class="d-flex justify-center align-center no-decoration black--text flex-column"  >
              <img src="../../assets/dataacademy.svg" alt="dataacademy-ico" height="150">
              <h3 style="margin-top:4px;">Data Academy</h3>
            </router-link>
          </v-flex>
        </v-layout>
       </v-container>
    </v-layout>
    <PageBreak/>
     <v-layout row section events justify-center>
       <v-container>
         <v-layout row justify-center>
          <h1 class="futura-lt bold heading">
            Events
          </h1>
         </v-layout>
        <v-layout row justify-center mt-4>
          <router-link to="/event/festival" class="d-flex justify-center align-center no-decoration black--text mr-4 flex-column" >
            <img src="https://static.arkavidia.id/5/images/icons/itfestival.svg" alt="itfest-ico" height="150">
            <h3 style="margin-top:4px;">IT Festival</h3>
          </router-link>
          <router-link to="/event/arkavtalk" class="d-flex justify-center align-center no-decoration black--text ml-4 flex-column"  >
            <img src="https://static.arkavidia.id/5/images/icons/seminar.svg" alt="seminar-ico" height="150">
            <h3 style="margin-top:4px;">ArkavTalk</h3>
          </router-link>
        </v-layout>
       </v-container>
    </v-layout>
    <PageBreak/>
    <v-layout row section competitions justify-center>
      <v-container justify-center>
        <v-layout row justify-center>
          <h1 class="futura-lt bold heading">
            Competitions
          </h1>
        </v-layout>
        <v-layout row justify-center style="margin-top:30px;">
        <v-flex md10 sm8 xs12 justify-center>
        <v-layout row justify-center wrap>
          <v-flex md3 xs6>
          <router-link to="/competition/cp" class="d-flex justify-center align-center no-decoration black--text flex-column" >
            <img src="https://static.arkavidia.id/5/images/icons/cp.svg" alt="cp-ico" height="120">
            <h3 style="margin-top:4px; text-align:center" class="competition-text">Competitive Programming</h3>
          </router-link>
          </v-flex>
          <v-flex md3 xs6>
          <router-link to="/competition/technovation" class="d-flex justify-center align-center no-decoration black--text flex-column" >
            <img src="https://static.arkavidia.id/5/images/icons/technovation.svg" alt="technovation-ico" height="120">
            <h3 style="margin-top:4px; text-align:center" class="competition-text">Technovation</h3>
          </router-link>
          </v-flex>
          <v-flex md3 xs6>
          <router-link to="/competition/ctf" class="d-flex justify-center align-center no-decoration black--text flex-column" >
            <img src="https://static.arkavidia.id/5/images/icons/ctf.svg" alt="ctf-ico" height="120">
            <h3 style="margin-top:4px; text-align:center;" class="competition-text">Capture the Flag</h3>
          </router-link>
          </v-flex>
          <v-flex md3 xs6>
          <router-link to="/competition/arkalogica" class="d-flex justify-center align-center no-decoration black--text flex-column" >
            <img src="https://static.arkavidia.id/5/images/icons/arkalogica.svg" alt="arkalogica-ico" height="120">
            <h3 style="margin-top:4px; text-align:center" class="competition-text">Arkalogica</h3>
          </router-link>
          </v-flex>
        </v-layout>
        </v-flex>
        </v-layout>
      </v-container>
    </v-layout>
    <!-- <v-layout row section competitions justify-center>
      <v-container justify-center>
        <v-layout row justify-center style="margin-bottom:30px;">
        <v-flex md10 sm8 xs12 justify-center>
        <v-layout row justify-center wrap>
          <a href="https://dashboard.arkavidia.id/register" class="no-decoration">
            <v-btn class="box-stroke">Register Now
            </v-btn>
          </a>
        </v-layout>
        </v-flex>
        </v-layout>
      </v-container>
    </v-layout> -->
    <!-- <PageBreak/>
     <v-layout row section schedule justify-center>
      <h1 class="futura-lt bold heading">
        Schedule
      </h1>
    </v-layout> -->
  </v-container>
</template>

<script>
import PageBreak from '@/components/partials/PageBreak'
import Countdown from 'vuejs-countdown'
export default {
  name: 'Home',
  components: {
    PageBreak, Countdown
  },
  props: {
    msg: String
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
.landing {
  width: 100%;
  position: relative;
}
.landing>div{
   background-image: url('https://static.arkavidia.id/5/images/landing-bg-2.svg');
  background-size: 102%;
  background-position: bottom;
}
.competition-text {
  display: flex;
  height: 50px;
  justify-content:center;
  align-items:center;
}
.bordered {
  border: 2px solid #04464F;
  padding: 10px;
  border-radius: 5px;
}

</style>
