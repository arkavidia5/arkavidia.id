<template>
  <v-container fluid no-padding>
    <!-- Hero -->
    <v-container fluid no-padding>
      <v-layout row fill-height fill-width id="jumbotron">
        <v-flex xl6 lg6 md6>
          <v-layout row style="height: 100%">
            <v-flex xl5 lg5 md5 id="ggj-jumboempty"/>
            <v-flex xl7 lg7 md7 id="ggj-jumbo">
              <div id="ggj-jumbo_overlay"/>
            </v-flex>
          </v-layout>
        </v-flex>
        <v-flex xl6 lg6 md6 id="ggj-title">
          <div class="heading-title heading-medium">
            <h1 class="heading-yellow futura-bt">CODING<br>CLASS</h1>
            <h1 class="shadow futura-bt">CODING<br>CLASS</h1>
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
    <v-container fluid id="gamejam-details">
      <!-- 1st row -->
      <v-layout row wrap id="gamejam-sec1">
        <v-flex xl4 lg4 md4 sm12 id="ggj-img">
          <div id="ggj-g1"/>
          <div id="ggj-g2"/>
          <div id="ggj-g3"/>
        </v-flex>
        <v-flex xl8 lg8 md8 id="gamejam-content">
          <div class="text-xs-justify" style="margin-left: 8px">
            <p>Coding Class merupakan sebuah Workshop Web Development yang dilakukan selama dua hari berturut-turut. Pada acara ini, peserta akan mendapatkan materi mengenai dasar-dasar web development serta seminar yang akan membuka wawasan mengenai web development. Target peserta adalah siswa tingkat SMA. Peserta dialokasikan ke suatu tim dengan satu mentor. Mentor akan mengawal keberjalanan class hingga peserta berhasil membuat demo dari produk terkait web. Harapan camp ini adalah siswa SMA di Indonesia dapat memiliki skill yang berguna dalam mengeksplorasi dunia IT dalam Revolusi Industri 4.0 saat ini.</p>
          </div>
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
      <v-layout row id="gamejam-sec2">
        <v-flex xl4 lg4 id="ggj-yellow"/>
        <v-flex xl8 lg8 id="ggj-yellow_img">
          <div/>
        </v-flex>
      </v-layout>
    </v-container>
  </v-container>
</template>

<script>
export default {
  name: 'Codingclass',
};
</script>

<style scoped>
@media only screen and (max-width: 767px) {
  #ggj-title {
    margin-top: 50px;
    padding-left: 10px;
    display: inline;
    z-index: 2;
  }
  #ggj-jumbo {
    /* width: 200px; */
    width: 100%;
    max-width: 767px;
    height: 100%;
    background: url('../../assets/codingclass-main.jpg') no-repeat center;
    background-size: auto 100%;
    display: inline;
    margin-left: 50px;
    z-index: 1;
    position: absolute;
  }

  #ggj-jumboempty {
    width: 25%;
    height: 100%;
    padding-right: -10px;
  }
  .view-more {
    margin-top: 10px;
  }

   #gamejam-details {
    /* height: 100vh; */
  }
  #ggj-img {
    height: 400px;
    width: 767px;
    display: inline;
    margin: 0 auto;
    margin-bottom: 20px;
    margin-left: 0;
    margin-right: 0;
    display:block;
    margin-top: -16px;
    vertical-align: middle;
  }
    #ggj-img > #ggj-g1 {
    height: calc(100% / 3);
    width: 100%;
    max-width: 767px;
    background: url('../../assets/codingclass-g1.jpg') no-repeat center;
    background-size: 100% auto;
    display: inline-block;
    vertical-align: middle;
  }

      #ggj-img > #ggj-g2 {
    height: calc(100% / 3);
    width: 100%;
    max-width: 767px;
    background: url('../../assets/codingclass-g2.jpg') no-repeat;
    background-size: 105% auto;
    background-position: left center;
    display: inline-block;
    vertical-align: middle;
  }

  #ggj-img > #ggj-g3 {
    height: calc(100% / 3);
    width: 100%;
    max-width: 767px;
    background: url('../../assets/codingclass-g3.jpg') no-repeat center;
    background-size: 100% auto;
    display: inline-block;
    vertical-align: middle;
  }
  #gamejam-details .container-fluid {
  padding-right: 15px;
  padding-left: 15px;
  margin-right: auto;
  margin-left: auto;
  padding: 0px;
}
#gamejam-details .row {
  margin-right: -15px;
  margin-left: -15px;
}
  #gamejam-content {
  width: 100%;
  justify-content: center;
  align-content: center;
  padding: 0 20% 0 5%;
  font-size: 1.1em;
  color: #094260;
  display: inline-block;
}
  #gamejam-sec2 {
    height: 25%;

  }
      #ggj-yellow_img {
        height: 100px;
            width: 100%;
    max-width: 767px;
    background: url('../../assets/codingclass-g4.jpg') no-repeat;
    background-size: 100% auto;
    background-position: 50% 90%;
  }
}



@media only screen and (min-width: 768px) {
  #ggj-title {
    padding-left: 40px;
  }
  #ggj-jumbo {
    height: 100%;
    background: url('../../assets/codingclass-main.jpg') no-repeat center;
    background-size: auto 100%;
  }
  #ggj-jumboempty {
    height: 100%;
  }
  .view-more {
    margin-top: 20px;
  }

  #gamejam-details {
    height: 100vh;
  }
    #ggj-img > #ggj-g1 {
    height: calc(100% / 3);
    background: url('../../assets/codingclass-g1.jpg') no-repeat center;
    background-size: 120% auto;
  }

  #ggj-img > #ggj-g2 {
    height: calc(100% / 3);
    background: url('../../assets/codingclass-g2.jpg') no-repeat;
    background-size: 105% auto;
    background-position: left center;
  }

  #ggj-img > #ggj-g3 {
    height: calc(100% / 3);
    background: url('../../assets/codingclass-g3.jpg') no-repeat center;
    background-size: 100% auto;
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
  #gamejam-sec2 {
    height: 25%;
  }
      #ggj-yellow_img {
    background: url('../../assets/codingclass-g4.jpg') no-repeat;
    background-size: 100% auto;
    background-position: 50% 90%;
  }
}

#jumbotron {
  height: 100vh;
  margin-top: 0 !important;
  background-image: url("../../assets/event_variation-01.svg");
  background-size: auto 40%;
  background-position: left 8vw center;
  position: relative;
  overflow: hidden;
}

#ggj-jumbo_overlay {
  background: rgba(248, 244, 1, 0.65);
  overflow: hidden;
  height: 100%;
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

#ggj-yellow {
  height: 100%;
  background-color: yellow;
}

#ggj-yellow_img  > div {
  background: rgba(248, 244, 1, 0.65);
  overflow: hidden;
  height: 100%;
}

</style>
