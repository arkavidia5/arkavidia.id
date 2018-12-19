<template>
  <v-container fluid no-padding id="gamejam" class="preevent">
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
            <h1 class="heading-yellow futura-bt">GLOBAL<br>GAME<br>JAM</h1>
            <h1 class="shadow futura-bt">GLOBAL<br>GAME<br>JAM</h1>
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
            <p>Di era digital ini sudah banyak bidang yang berkembang pesat. Tak terkecuali bidang game development. Banyak sekali developer game yang memiliki minat untuk mengembangkan game namun tidak mendapatkan ruang untuk menampilkan hasil kreasi mereka. Global Game Jam dapat menjadi wadah bagi anda yang tertarik untuk menampilkan hasil karya terbaik anda di bidang game development. Global Game Jam merupakan acara tahunan yang diadakan di seluruh dunia, tak terkecuali di kota Bandung. Peserta lomba saling berlomba satu sama lain dalam membuat sebuah game dengan tema tertentu.</p>
          </div>
          <v-flex md1 xs12>
            <a href="https://bit.ly/GGJ-ITB-2019" class="no-decoration" target='_blank'>
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
      <!-- 2nd row -->
      <v-layout row id="preevent-sec2">
        <v-flex xl4 lg4 id="preevent-yellow"/>
        <v-flex xl8 lg8 id="preevent-yellow_img">
          <div/>
        </v-flex>
      </v-layout>
    </v-container>
  </v-container>
</template>

<script>
export default {
  name: 'Gamejam',
};
</script>

<style scoped>
@media only screen and (max-width: 767px) {
  .preevent#gamejam #preevent-title {
    padding-left: 10px;
    display: inline;
    z-index: 2;
  }
  .preevent #preevent-jumbo {
    width: 100%;
    max-width: 767px;
    height: 100%;
    background: url('../../assets/ggj-main.jpg') no-repeat center;
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
    background: url('../../assets/ggj-g1.jpg') no-repeat center;
    background-size: 100% auto;
    display: inline-block;
    vertical-align: middle;
  }

  .preevent #preevent-img > #preevent-g2 {
    height: calc(100% / 3);
    width: 100%;
    max-width: 767px;
    background: url('../../assets/ggj-g2.jpg') no-repeat;
    background-size: 105% auto;
    background-position: left center;
    display: inline-block;
    vertical-align: middle;
  }

  .preevent #preevent-img > #preevent-g3 {
    height: calc(100% / 3);
    width: 100%;
    max-width: 767px;
    background: url('../../assets/ggj-g3.jpg') no-repeat center;
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
  .preevent #preevent-sec2 {
    height: 25%;
  }
  .preevent #preevent-yellow_img {
    height: 100px;
    width: 100%;
    max-width: 767px;
    background: url('../../assets/ggj-g4.jpg') no-repeat;
    background-size: 100% auto;
    background-position: 50% 90%;
  }
}



@media only screen and (min-width: 768px) {
  .preevent #preevent-title {
    padding-left: 40px;
  }
  .preevent #preevent-jumbo {
    height: 100%;
    background: url('../../assets/ggj-main.jpg') no-repeat center;
    background-size: auto 100%;
  }
  .preevent #preevent-jumboempty {
    height: 100%;
  }
  .preevent .view-more {
    margin-top: 20px;
  }

  .preevent #preevent-details {
    height: 100vh;
  }
   .preevent #preevent-img > #preevent-g1 {
    height: calc(100% / 3);
    background: url('../../assets/ggj-g1.jpg') no-repeat center;
    background-size: 120% auto;
  }

  .preevent #preevent-img > #preevent-g2 {
    height: calc(100% / 3);
    background: url('../../assets/ggj-g2.jpg') no-repeat;
    background-size: 105% auto;
    background-position: left center;
  }

  .preevent #preevent-img > #preevent-g3 {
    height: calc(100% / 3);
    background: url('../../assets/ggj-g3.jpg') no-repeat center;
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
  .preevent #preevent-sec2 {
    height: 25%;
  }
  .preevent #preevent-yellow_img {
    background: url('../../assets/ggj-g4.jpg') no-repeat;
    background-size: 100% auto;
    background-position: 50% 90%;
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
  top: 48vh;
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
/* #jumbotron {
  height: 100vh;
  margin-top: 0 !important;
  background-image: url("../../assets/event_variation-01.svg");
  background-size: auto 40%;
  background-position: left 8vw center;
  position: relative;
}

#ggj-jumboempty {
  height: 100%;
}

#ggj-jumbo {
  height: 100%;
  background: url('../../assets/ggj-main.jpg') no-repeat center;
  background-size: auto 100%;
}

#ggj-jumbo_overlay {
  background: rgba(248, 244, 1, 0.65);
  overflow: hidden;
  height: 100%;
}

#ggj-title {
  padding-left: 40px;
}

#gamejam-details {
  height: 100vh;
}

#gamejam-content {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-content: center;
  padding: 0 20% 0 5%;
  font-size: 1.1em;
  color: #094260;
}

.heading-title {
  font-weight: bold;
  top: 48vh;
  position: relative;
  min-width: 240px;
  line-height: 2em;
  letter-spacing: -3px;
}

.heading-title > .heading-yellow {
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

.heading-title > .shadow {
  color: #1DE9EB;
  -webkit-text-stroke-width: 2px;
  -webkit-text-stroke-color: #094260;
  display: inline-block;
  z-index: 2;
}

.view-more {
  position: absolute;
  bottom: 10vh;
  margin-left: 120px;
  width: 100%;
}

.view-more > .chevron {
  background: #FFD900;
  padding: 0px 16px 0px 16px;
  border: 2px solid #094260;
  border-radius: 4px;
  margin-top: 8px;
  display: inline-block;
  cursor: pointer;
}

.mid-button-group {
  display: inline-block;
  position: relative;
  padding-top: 24px;
}

.mid-button-group > .btn-line {
  border: 2px solid #094260;
  width: 60px;
  position: absolute;
  top: 0;
  left: 0;
}

#gamejam-sec1 {
  height: 75%;
  display: flex;
  flex-direction: row;
}

#gamejam-sec2 {
  height: 25%;
}

#ggj-img > #ggj-g1 {
  height: calc(100% / 3);
  background: url('../../assets/ggj-g1.jpg') no-repeat center;
  background-size: 120% auto;
}

#ggj-img > #ggj-g2 {
  height: calc(100% / 3);
  background: url('../../assets/ggj-g2.jpg') no-repeat;
  background-size: 105% auto;
  background-position: left center;
}

#ggj-img > #ggj-g3 {
  height: calc(100% / 3);
  background: url('../../assets/ggj-g3.jpg') no-repeat center;
  background-size: 100% auto;
}

#ggj-yellow {
  height: 100%;
  background-color: yellow;
}

#ggj-yellow_img {
  background: url('../../assets/ggj-g4.jpg') no-repeat;
  background-size: 100% auto;
  background-position: 50% 90%;
}
#ggj-yellow_img  > div {
  background: rgba(248, 244, 1, 0.65);
  overflow: hidden;
  height: 100%;
} */

</style>
