<template>
  <v-container fluid no-padding>
    <v-container fluid no-padding>
      <v-layout row align-center justify-center fill-height fill-width id="arkavtalk-jumbotron">
        <v-flex>
          <div align="center">
            <b style="letter-spacing: 4px;">ARKAVIDIA 5.0 PRESENTS</b>
            <div class="heading-title">
              <h1 class="heading-yellow heading-xlarge margin-bottom-sm futura-bt">ARKAVTALK</h1>
              <h1 class="shadow heading-xlarge margin-bottom-sm futura-bt">ARKAVTALK</h1>
            </div>
            <div class="view-more">
              <div class="futura-bt" style="letter-spacing: 4px; color: #FFD900">VIEW MORE</div>
              <div class="chevron futura-bt" v-scroll-to="'#arkavtalk-details'">
                <i class="material-icons">keyboard_arrow_down</i>
              </div>
            </div>
          </div>
        </v-flex>
      </v-layout>
    </v-container>
    <v-container fluid id="arkavtalk-details">
      <v-container class="content">
        <v-layout row class="mt-5 mb-5">
          <v-flex xs1/>
          <v-flex xs12>
            <!-- <p class="text-xs-justify" style="font-size: 1.3rem">
              ArkavTalk adalah salah satu rangkaian acara dari main event ARKAVIDIA 5.0. ArkavTalk kali ini dibagi menjadi dua topik besar, yang pertama adalah topik tentang pendidikan di masa kini yang memanfaatkan teknologi informasi. Topik pertama ditujukan untuk setiap siswa dan mahasiswa yang menjadi pengguna langsung dari layanan educational technology. Topik kedua adalah perkembangan IT dalam bidang Artificial Intelligence, Big Data, Cloud Computing dan Cyber Security. ArkavTalk akan dibawakan oleh startup-startup IT yang bergerak di bidang pendidikan, dan startup-startup IT di bidang lainnya. Pendaftaran ArkavTalk akan dibuka pada bulan Januari 2019.
            </p> -->
            <div align="center">
              <!-- <div class="mid-button-group mt-3">
                <div class="btn-line mb-3 ml-2">
                  <h1>E</h1>
                </div>
              </div> -->
              <h1 class="heading-medium">Topics</h1>

              <br>
              <template id="sesi1">
                <h2 class="heading-small">Sesi 1</h2>
                <div class="heading small-text">9 Februari 2019, 08.30</div>
                <div class="heading small-text">Auditorium CC Timur, ITB Kampus Ganesha</div>
                <div class="heading small-text">HTM : Rp 20.000</div>
                <v-layout class="row">
                  <v-flex class="xs10 offset-xs1">
                    <v-layout class="row row-pembicara wrap">
                      <v-flex class="xs12 md4 pa-3">
                        <span class="heading small">Why Learning <br> Should Be <br> Your Lifestyle</span>
                        <div class="foto-pembicara">
                          <img src="https://static.arkavidia.id/5/images/logo.svg" alt="" >
                        </div>
                        <div class="heading small mt-2 mb-0"><b>Zaneti Sugiharti</b></div>
                        <div class="position-text">Head of Marketing & <br> Communications HarukaEDU</div>
                      </v-flex>
                      <v-flex class="xs12 md4 pa-3">
                        <span class="heading small">Set Up <br> Your Own Learning <br> Environment</span>
                        <div class="foto-pembicara">
                          <img src="https://static.arkavidia.id/5/images/logo.svg" alt="" >
                        </div>
                        <div class="heading small mt-2"><b>Tri Nuraini</b></div>
                        <div class="position-text">Head of PR & Marketing <br> Quipper Indonesia</div>

                      </v-flex>
                      <v-flex class="xs12 md4 pa-3">
                        <span class="heading small">Boost Your Learning <br> Experience With <br> Online Course</span>
                        <div class="foto-pembicara">
                          <img src="https://static.arkavidia.id/5/images/logo.svg" alt="" >
                        </div>
                        <div class="heading small mt-2"><b>Lucyanna Pandjaitan</b></div>
                        <div class="position-text">Presiden Direktur & <br> CEO IndonesiaX</div>

                      </v-flex>
                    </v-layout>
                  </v-flex>
                </v-layout>
                <br>
              </template>
              <template id="sesi2">
                <h2 class="heading-small">Sesi 2</h2>
                <div class="heading small-text">9 Februari 2019, 12.30</div>
                <div class="heading small-text">Auditorium CC Timur, ITB Kampus Ganesha</div>
                <div class="heading small-text">HTM : Rp 30.000</div>
                <v-layout class="row row-pembicara wrap">
                      <v-flex class="xs12 md3 pa-1">
                        <span class="heading small">How Data <br> Transform <br> Our Life</span>  
                          <div class="foto-pembicara">
                            <img src="https://static.arkavidia.id/5/images/logo.svg" alt="" >
                          </div>
                          <div class="heading small mt-2"><b>Syafri Bahar</b></div>
                          <div class="position-text">Vice President of <br> Data Science Go-Jek</div>
                      </v-flex>
                      <v-flex class="xs12 md3 pa-1">
                        <span class="heading small">Dive Inside <br> E-commerce <br> Recommendation System</span>  
                        <div class="foto-pembicara">
                          <img src="https://static.arkavidia.id/5/images/logo.svg" alt="" >
                        </div>
                        <div class="heading small mt-2"><b>Reza Aditya Permadi</b></div>
                        <div class="position-text">AI Research Manager <br> Bukalapak</div>

                      </v-flex>
                      <v-flex class="xs12 md3 pa-1">
                        <span class="heading small">Unboxing <br> E-commerce <br> Design Tricks</span>  
                        <div class="foto-pembicara">
                          <img src="https://static.arkavidia.id/5/images/logo.svg" alt="" >
                        </div>
                        <div class="heading small mt-2"><b>Adze Ganesha</b></div>
                        <div class="position-text">Product Design Expert (UX) <br> Tokopedia</div>

                      </v-flex>
                       <v-flex class="xs12 md3 pa-1">
                        <span class="heading small">Recent Technology <br> in Cloud Computing and <br> Its Impact to The Future </span>  
                        <div class="foto-pembicara">
                          <img src="https://static.arkavidia.id/5/images/logo.svg" alt="" >
                        </div>
                        <div class="heading small mt-2"><b>Eric Cahya</b></div>
                        <div class="position-text">Infrastructure Manager <br> Xtremax</div>

                      </v-flex>
                </v-layout>
                <br>
              </template>
              
            </div>
            <div align="right">
              <a href="https://dashboard.arkavidia.id/event/arkavtalk" class="no-decoration" target='_blank'>
                  <v-btn class="outlined-button futura-bt ma-2" style="font-size: 1.3rem" >Daftar Sekarang!</v-btn>
              </a>
            </div>
          </v-flex>
          <v-flex xl3 lg2 xs1/>
        </v-layout>
      </v-container>
    </v-container>
    <v-container fluid grid-list-md no-padding>
      <v-layout row wrap>
        <v-flex d-flex md4 xs12 class="img-sec" id="arkavtalk-img-l"></v-flex>
        <v-flex d-flex md4 xs12 class="img-sec">
          <v-container no-padding>
            <v-layout row fill-height>
              <v-flex d-flex xs12 class="img-sec-m" id="arkavtalk-img-mt"></v-flex>
            </v-layout>
            <v-layout row fill-height>
              <v-flex d-flex xs12 class="img-sec-m" id="arkavtalk-img-mb"></v-flex>
            </v-layout>
          </v-container>
        </v-flex>
        <v-flex d-flex md4 xs12 class="img-sec" id="arkavtalk-img-r"></v-flex>
      </v-layout>
    </v-container>
  </v-container>
</template>

<script>
  export default {
    name: 'Arkavtalk',
    props: {
      msg: String
    }
  }
</script>

<style type="text/css">
  #arkavtalk-jumbotron {
    height: 100vh;
    margin-top: 0 !important;
    background-image: url("../../assets/event_variation-01.svg"), url("../../assets/bg-arkavtalk.jpg");
    background-size: auto 40%, cover;
    background-position: left 8vw center, center;
    position: relative;
  }

  #arkavtalk-details {
    background-image: url('../../assets/bg_pattern.png') !important;
    background-size: 80%;
    background-position: top left;
    background-repeat: repeat;
  }

  #arkavtalk-details > .content {
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
    bottom: 80px;
    width: 100%;
  }

  .view-more > .chevron {
    background: #FFD900;
    padding: 0px 16px 0px 16px;
    border: 2px solid #094260;
    border-radius: 4px;
    margin-top: 8px;
    display: inline-flex;
    justify-content: center;
    align-items: center;
    cursor: pointer;
  }
  .view-more > .chevron > .material-icons {
    font-size: 2rem;
    display: block;
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

  .img-sec#arkavtalk-img-l {
    background-image: url("../../assets/arkavtalk-g2.jpg");
  }
  .img-sec#arkavtalk-img-r {
    background-image: url("../../assets/arkavtalk-g4.jpg");
  }
  .img-sec-m#arkavtalk-img-mt {
    background-image: url("../../assets/arkavtalk-g1.jpg");
    background-position: bottom;
    background-size: cover;
  }
  .img-sec-m#arkavtalk-img-mb {
    background-image: url("../../assets/arkavtalk-g3.jpg");
    background-position: top;
    background-size: cover;
  }

  @media only screen and (max-width: 500px) {
    #arkavtalk-jumbotron {
      background-image: url("../../assets/bg-arkavtalk.jpg");
      background-size: cover;
      background-position: center;
    }

    #arkavtalk-details > .content {
      background: none;
    }
  }
  .small-text {
    font-size: 1.5rem !important;
  }
  .foto-pembicara {
    border-radius: 50% ;
    height: 125px !important;
    width: 125px !important;
    object-fit: cover;
    border: 7px solid #04464F;
    background: white;
  }
  .foto-pembicara>img {
    max-height: 100%;
    max-width: 100%;
    object-fit: contain;
  }
  .row-pembicara {
    margin-top: 20px;
  }
  .heading.small {
    font-family: 'Futura Md BT Bold';
    font-weight: 900;
    font-size: 1.2rem;
  }
  .position-text {
    color: #137F7F;
    font-size: 0.9rem;
    line-height: 1 rem;
  }
</style>
