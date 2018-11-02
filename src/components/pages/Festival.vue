<template>
  <v-container fluid no-padding>
    <v-container fluid no-padding>
      <v-layout row align-center justify-center fill-height fill-width id="itfest-jumbotron">
        <v-flex>
          <div align="center">
            <b style="letter-spacing: 4px;">ARKAVIDIA 5.0 PRESENTS</b>
            <div class="heading-title">
              <h1 class="heading-yellow heading-xlarge margin-bottom-sm futura-bt">IT FESTIVAL</h1>
              <h1 class="shadow heading-xlarge margin-bottom-sm futura-bt">IT FESTIVAL</h1>
            </div>
            <div class="view-more">
              <div class="futura-bt" style="letter-spacing: 4px; color: #FFD900">VIEW MORE</div>
              <div class="chevron futura-bt" v-scroll-to="'#itfest-details'">
                V
              </div>
            </div>
          </div>
        </v-flex>
      </v-layout>
    </v-container>
    <v-container fluid id="itfest-details">
      <v-container class="content">
        <v-layout row class="mt-5 mb-5">
          <v-flex xl3 lg2 xs1/>
          <v-flex xl6 lg8 xs10>
            <p class="text-xs-justify" style="font-size: 1.3rem">
              IT-Festival ARKAVIDIA adalah salah satu rangkaian acara dari main event ARKAVIDIA 5.0. Acara ini menampilkan puluhan karya digital startup dari berbagai latar belakang seperti bidang pendidikan, e-commerce, fintech, dan berbagai bidang lainnya. IT-Festival ARKAVIDIA diselenggarakan oleh Himpunan Mahasiswa Informatika, Program Studi Teknik Informatika, dan Program Studi Sistem dan Teknologi Informasi Institut Teknologi Bandung. Dalam IT-Festival ARKAVIDIA, pengunjung dapat menggali informasi, melihat produk-produk inovatif terbaru, berinteraksi secara langsung teknologi-teknologi terkini, juga menikmati makanan di foodcourt yang sediakan. Dengan diadakannya IT-Festival ini, diharapkan masyarakat dapat mengenal karya pelaku industri kreatif dan terinspirasi untuk berkarya di Indonesia.
            </p>
            <div align="center">
              <div class="mid-button-group mt-3">
                <div class="btn-line mb-3 ml-2"></div>
                <button class="outlined-button futura-bt ma-2" style="font-size: 1.3rem">Unduh Rulebook</button>
                <button class="outlined-button futura-bt ma-2" style="font-size: 1.3rem">Daftar Sekarang!</button>
              </div>
            </div>
          </v-flex>
          <v-flex xl3 lg2 xs1/>
        </v-layout>
      </v-container>
    </v-container>
    <v-container fluid grid-list-md no-padding>
      <v-layout row wrap>
        <v-flex d-flex md4 xs12 class="img-sec" id="itfest-img-l"></v-flex>
        <v-flex d-flex md4 xs12 class="img-sec">
          <v-container no-padding>
            <v-layout row fill-height>
              <v-flex d-flex xs12 class="img-sec-m" id="itfest-img-mt"></v-flex>
            </v-layout>
            <v-layout row fill-height>
              <v-flex d-flex xs12 class="img-sec-m" id="itfest-img-mb"></v-flex>
            </v-layout>
          </v-container>
        </v-flex>
        <v-flex d-flex md4 xs12 class="img-sec" id="itfest-img-r"></v-flex>
      </v-layout>
    </v-container>
  </v-container>
</template>

<script>
  import Vue from 'vue';
  import VueScrollTo from 'vue-scrollto';
export default {
  name: 'Festival',
  props: {
    msg: String
  },
    components: {
        VueScrollTo, Vue
    }
}

</script>
<style type="text/css">
  #itfest-jumbotron {
    height: 100vh;
    margin-top: 0 !important;
    background-image: url("../../assets/event_variation-01.svg"), url("../../assets/bg-itfest.jpg");
    background-size: auto 40%, cover;
    background-position: left 8vw center, center;
    position: relative;
  }

  #itfest-details {
    background-image: url('../../assets/bg_pattern.png') !important;
    background-size: 80%;
    background-position: top left;
    background-repeat: repeat;
  }

  #itfest-details > .content {
    background-image: url("../../assets/3dots.svg");
    background-size: 40px auto;
    background-position: right 20px center;
    background-repeat: no-repeat;
  }

  .heading-title {
    position: relative;
    min-width: 240px;
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
    bottom: 32px;
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

  .img-sec {
    height: 400px;
    background-size: cover;
    background-position: center;
  }

  .img-sec-m {
    height: 200px;
  }

  .img-sec#itfest-img-l {
    background-image: url("../../assets/itfest-g2.jpg");
  }
  .img-sec#itfest-img-r {
    background-image: url("../../assets/itfest-g4.jpg");
  }
  .img-sec-m#itfest-img-mt {
    background-image: url("../../assets/itfest-g1.jpg");
    background-position: bottom;
    background-size: cover;
  }
  .img-sec-m#itfest-img-mb {
    background-image: url("../../assets/itfest-g3.jpg");
    background-position: top;
    background-size: cover;
  }

  @media only screen and (max-width: 500px) {
    #itfest-jumbotron {
      background-image: url("../../assets/bg-itfest.jpg");
      background-size: cover;
      background-position: center;
    }

    #itfest-details > .content {
      background: none;
    }
  }
</style>