<template>
  <v-container fluid no-padding id="dataacademy" class="preevent">
    <!-- Hero -->
    <v-container fluid no-padding>
      <v-layout row fill-height fill-width id="jumbotron">
        <v-flex xl6 lg6 md6>
          <v-layout row style="height: 100%">
            <v-flex xl5 lg5 md5 id="preevent-jumboempty"/>
            <v-flex xl7 lg7 md7 id="preevent-jumbo">
              <div id="preevent-jumbo_overlay"/>
            </v-flex>
          </v-layout>
        </v-flex>
        <v-flex xl6 lg6 md6 id="preevent-title">
          <div class="heading-title heading-medium">
            <h1 class="heading-yellow futura-bt">DATA<br>ACADEMY</h1>
            <h1 class="shadow futura-bt">DATA<br>ACADEMY</h1>
            <br/>
            <h5 class="shadow futura-bt">IN COLLABORATION WITH</h5>
            <img src="../../assets/gojek.png" alt="gojek-ico" height="50px" style="margin-top: 0px; display:block;">
          </div>
          <div class="view-more">
            <div class="futura-bt" style="letter-spacing: 4px; color: #094260">VIEW MORE</div>
            <div class="chevron futura-bt" v-scroll-to="'#itfest-details'">
              <v-icon>keyboard_arrow_down</v-icon>
            </div>
          </div>
        </v-flex>
      </v-layout>
    </v-container>
    <!-- Details -->
    <v-container fluid id="preevent-details">
      <!-- 1st row -->
      <v-layout row wrap id="preevent-sec1">
        <v-flex xl4 lg4 md4 sm12 id="preevent-img">
          <div id="preevent-g1"/>
          <div id="preevent-g2"/>
          <div id="preevent-g3"/>
        </v-flex>
        <v-flex xl8 lg8 md8 id="preevent-content">
          <div class="text-xs-justify" style="margin-left: 8px">
            <p>Data Academy merupakan sebuah acara yang akan mengajarkanmu mempelajari dan menyelesaikan suatu masalah dengan data processing yang baik. Dalam acara ini, kalian akan mendapatkan berbagai seminar tentang data science dari pembicara-pembicara terkemuka, juga praktik data dashboarding maupun preprocessing.</p>
          </div>
            <v-flex md1 xs12>
            <a href="https://bit.ly/DataAcademy2019" class="no-decoration" target='_blank'>
             <v-btn class="box-stroke" >Daftar Sekarang!</v-btn>
            </a>
          </v-flex>

          <div>
            <div class="mid-button-group mt-3">
              <div class="btn-line mb-3 ml-2"></div>
              <!-- <button class="outlined-button futura-bt ma-2" style="font-size: 1.3rem">Unduh Rulebook</button>
              <button class="outlined-button futura-bt ma-2" style="font-size: 1.3rem">Daftar Sekarang!</button> -->
            </div>
          </div>
        </v-flex>
      </v-layout>
    </v-container>
    <!-- Timeline -->
    <v-container fluid id="preevent-timeline">
      <v-layout row margin-bottom-xl class="page-margin">
        <v-flex sm12 xs12>
          <v-layout row>
            <v-flex sm12 xs12 offset-md1>
              <h1 class="sherpa-blue heading-small shadow-yellow margin-bottom-sm" align="left">TIMELINE KEGIATAN</h1>
              <!-- <svg class="dash-height dash-fill margin-bottom-xs">
                <rect width="20%" height="100%"/>
              </svg> -->
              <v-layout row class="dash-size line-fill margin-bottom-sm">
              </v-layout>
            </v-flex>
          </v-layout>
          <v-layout row>
            <Timeline>
              <TimelineItem direction="right" image="https://static.arkavidia.id/5/images/icons/competition/icon_pendaftaran.svg" title="PENDAFTARAN" time="11 - 17 Januari 2019" description="Pendaftaran"/>
              <TimelineItem direction="left" image="https://static.arkavidia.id/5/images/icons/competition/icon_type.svg" title="BABAK INTERVIEW" time="18 - 23 Januari 2019" description="Interview calon peserta lomba"/> 
              <TimelineItem direction="right" image="https://static.arkavidia.id/5/images/icons/competition/icon_pengumuman.svg" title="PENGUMUMAN PESERTA" time="28 Januari 2019" description="Pengumuman peserta"/> 
              <TimelineItem direction="left" image="https://static.arkavidia.id/5/images/icons/competition/icon_podium.svg" title="ACARA" time="2 - 3 Februari 2019" description="Data Academy"/> 
            </Timeline>
          </v-layout>    
        </v-flex>
      </v-layout>
    </v-container>
      <!-- /Timeline -->
  </v-container>
</template>

<script>
import Timeline from '../partials/Timeline'
import TimelineItem from '../partials/TimelineItem'

export default {
  name: 'Dataacademy',
  components: {
    Timeline,
    TimelineItem
  },
  props: {
    msg: String
  }
};
</script>

<style scoped>
@media only screen and (max-width: 767px) {
  .preevent#dataacademy #preevent-title {
    margin-top: 50px;
    padding-left: 10px;
    display: inline;
    z-index: 2;
  }
  .preevent #preevent-jumbo {
    /* width: 200px; */
    width: 100%;
    max-width: 767px;
    height: 100%;
    background: url('../../assets/data-main.jpg') no-repeat center;
    background-size: auto 100%;
    display: inline;
    margin-left: 50px;
    z-index: 1;
    position: absolute;
  }

  .preevent #preevent-jumboempty {
    width: 25%;
    height: 100%;
    padding-right: -10px;
  }
  .preevent  .view-more {
    margin-top: 10px;
  }
  .preevent #preevent-details {
    /* height: 100vh; */
  }
  .preevent #preevent-img {
    height: 400px;
    width: 767px;
    display: inline;
    margin: 0 auto;
    margin-bottom: 20px;
    margin-left: 0;
    margin-right: 0;
    display:block;
    margin-top: 30px;
    vertical-align: middle;
  }
  .preevent #preevent-img > #preevent-g1 {
    height: calc(100% / 3);
    width: 100%;
    max-width: 767px;
    background: url('../../assets/data-g1.jpg') no-repeat center;
    background-size: 100% auto;
    display: inline-block;
    vertical-align: middle;
  }

  .preevent #preevent-img > #preevent-g2 {
    height: calc(100% / 3);
    width: 100%;
    max-width: 767px;
    background: url('../../assets/data-g2.jpg') no-repeat;
    background-size: 105% auto;
    background-position: left center;
    display: inline-block;
    vertical-align: middle;
  }

  .preevent #preevent-img > #preevent-g3 {
    height: calc(100% / 3);
    width: 100%;
    max-width: 767px;
    background: url('../../assets/data-g3.jpg') no-repeat center;
    background-size: 100% auto;
    display: inline-block;
    vertical-align: middle;
  }
  .preevent #preevent-details .container-fluid {
    padding-right: 15px;
    padding-left: 15px;
    margin-right: auto;
    margin-left: auto;
    padding: 0px;
  }
 .preevent #preevent-details .row {
    margin-right: -15px;
    margin-left: -15px;
  }
  .preevent #preevent-content {
    width: 100%;
    justify-content: center;
    align-content: center;
    padding: 0 20% 0 5%;
    font-size: 1.1em;
    color: #094260;
    display: inline-block;
  }
}



@media only screen and (min-width: 768px) {
  .preevent #preevent-title {
    padding-left: 40px;
  }
  .preevent #preevent-jumbo {
    height: 100%;
    background: url('../../assets/data-main.jpg') no-repeat center;
    background-size: auto 100%;
  }
  .preevent #preevent-jumboempty {
    height: 100%;
  }
  .preevent .view-more {
    margin-top: 20px;
  }

  .view-more {
    position: absolute;
    bottom: 10px;
    width: 100%;
  }

  .preevent #preevent-details {
    height: 100vh;
  }
  .preevent #preevent-timeline {
      margin-top: -20vh;
  }
   .preevent #preevent-img > #preevent-g1 {
    height: calc(100% / 3);
    background: url('../../assets/data-g1.jpg') no-repeat center;
    background-size: 120% auto;
  }

  .preevent #preevent-img > #preevent-g2 {
    height: calc(100% / 3);
    background: url('../../assets/data-g2.jpg') no-repeat;
    background-size: 105% auto;
    background-position: left center;
  }

  .preevent #preevent-img > #preevent-g3 {
    height: calc(100% / 3);
    background: url('../../assets/data-g3.jpg') no-repeat center;
    background-size: 100% auto;
  }

  .preevent #preevent-content {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-content: center;
    padding: 0 20% 0 5%;
    font-size: 1.1em;
    color: #094260;
  }
}

.preevent #jumbotron {
  height: 100vh;
  margin-top: 0 !important;
  background-image: url("../../assets/event_variation-01.svg");
  background-size: auto 40%;
  background-position: left 8vw center;
  position: relative;
  overflow: hidden;
}

.preevent #preevent-jumbo_overlay {
  background: rgba(248, 244, 1, 0.65);
  overflow: hidden;
  height: 100%;
  }
.preevent .view-more > .chevron {
  background: #FFD900;
  padding: 0px 16px 0px 16px;
  border: 2px solid #094260;
  border-radius: 4px;
  margin-top: 8px;
  display: inline-block;
  cursor: pointer;
}

.preevent .heading-title {
  font-weight: bold;
  top: 40vh;
  position: relative;
  min-width: 240px;
  line-height: 2em;
  letter-spacing: -3px;
}

.preevent .heading-title > .heading-yellow {
  color: #FFD900;
  -webkit-text-stroke-width: 2px;
  -webkit-text-stroke-color: #094260;
  position: absolute;
  margin-top: 5px;
  margin-left: 5px;
  top: auto;
  left: auto;
  width: auto;
  display: inline-block;
}

.preevent .heading-title > .shadow {
  color: #1DE9EB;
  -webkit-text-stroke-width: 2px;
  -webkit-text-stroke-color: #094260;
  display: inline-block;
  z-index: 2;
}

.preevent .mid-button-group {
  display: inline-block;
  position: relative;
  padding-top: 24px;
}

.preevent .mid-button-group > .btn-line {
  border: 2px solid #094260;
  width: 60px;
  position: absolute;
  top: 0;
  left: 0;
}

.preevent #preevent-sec1 {
  height: 75%;
  display: flex;
  flex-direction: row;
}

.preevent #preevent-yellow {
  height: 100%;
  background-color: yellow;
}

.preevent #preevent-yellow_img  > div {
  background: rgba(248, 244, 1, 0.65);
  overflow: hidden;
  height: 100%;
}
</style>
