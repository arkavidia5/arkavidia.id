<template>
  <v-container fluid no-padding>
    <!-- Hero -->
    <v-container fluid no-padding>
      <v-layout row id="jumbotron">
        <v-flex xl6>
          <v-layout row style="height: 100%">
            <v-flex xl5 id="ggj-jumboempty"/>
            <v-flex xl7 id="ggj-jumbo">
              <div id="ggj-jumbo_overlay"/>
            </v-flex>
          </v-layout>
        </v-flex>
        <v-flex xl6 id="ggj-title">
          <div class="heading-title heading-medium">
            <h1 class="heading-yellow futura-bt">GLOBAL<br>GAME<br>JAM</h1>
            <h1 class="shadow futura-bt">GLOBAL<br>GAME<br>JAM</h1>
          </div>
          <div class="view-more">
            <div class="futura-bt" style="letter-spacing: 4px; color: #094260">VIEW MORE</div>
            <div class="chevron futura-bt" v-scroll-to="'#itfest-details'">
              V
            </div>
          </div>
        </v-flex>
      </v-layout>
    </v-container>
    <!-- Details -->
    <v-container fluid no-padding id="gamejam-details">
      <!-- 1st row -->
      <v-layout row id="gamejam-sec1">
        <v-flex xl4 id="ggj-img">
          <div id="ggj-g1"/>
          <div id="ggj-g2"/>
          <div id="ggj-g3"/>
        </v-flex>
        <v-flex xl8 id="gamejam-content">
          <div class="text-xs-justify" style="margin-left: 8px">
            <p>Di era digital ini sudah banyak bidang yang berkembang pesat. Tak terkecuali bidang game development. Banyak sekali developer game yang memiliki minat untuk mengembangkan game namun tidak mendapatkan ruang untuk menampilkan hasil kreasi mereka. Global Game Jam dapat menjadi wadah bagi anda yang tertarik untuk menampilkan hasil karya terbaik anda di bidang game development. Global Game Jam merupakan acara tahunan yang diadakan di seluruh dunia, tak terkecuali di kota Bandung. Peserta lomba saling berlomba satu sama lain dalam membuat sebuah game dengan tema tertentu.</p>
          </div>
          <div>
            <div class="mid-button-group mt-3">
              <div class="btn-line mb-3 ml-2"></div>
              <button class="outlined-button futura-bt ma-2" style="font-size: 1.3rem">Unduh Rulebook</button>
              <button class="outlined-button futura-bt ma-2" style="font-size: 1.3rem">Daftar Sekarang!</button>
            </div>
          </div>
        </v-flex>
      </v-layout>
      <!-- 2nd row -->
      <v-layout row id="gamejam-sec2">
        <v-flex xl4 id="ggj-yellow"/>
        <v-flex xl8 id="ggj-yellow_img">
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
#jumbotron {
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
}

</style>
