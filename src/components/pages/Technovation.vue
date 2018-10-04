<template>
  <v-container fluid>
    <v-slide-y-transition mode="out-in">
      <v-responsive :aspect-ratio="1.60 " class="row technovation-background">
        <v-container>
          <v-layout row margin-bottom-xl>
            <v-flex sm12 xs10 offset-xs1 >
                  <p class="text-stroke heading-medium line-height-small margin-bottom-none">Competition 
                    <span class="dash-box">_</span>
                  </p>
                  <h1 class="sherpa-blue heading-large shadow-yellow margin-bottom-sm" align="left">TECHNOVATION</h1>
                  <v-layout row>
                    <v-flex md9 xs8 class="d-flex flex-column">
                      <p class="content-text margin-bottom-xs">
                        Lomba Technovation merupakan lomba pengembangan ide perangkat luak yang dapat diikuti oleh setiap mahasiswa-mahasiswi di Indonesia. Titik berat pada lomba ini adalah ide yang inovatif, feasible, sustainable, dan seberapa besar manfaat yang diberikan untuk kemajuan Indonesia, terutama di bidang IT.
                      </p>
                      <!-- <svg class="dash-height dash-fill margin-bottom-sm">
                        <rect width="20%" height="100%"/>
                      </svg> -->
                      <v-layout row class="dash-size line-fill margin-bottom-sm">
                      </v-layout>
                      <v-layout row>
                        <v-btn class="box-stroke">Unduh Rulebook
                        </v-btn>
                        <v-btn class="box-stroke">Daftar Sekarang!
                        </v-btn>
                      </v-layout>

                    </v-flex>
                    <v-flex md3 xs4 class="d-flex flex-column">
                      <img src="../../assets/tower.svg" alt="technovation-ico" height="200rem">
                    </v-flex>
                  </v-layout>
            </v-flex>
          </v-layout>
          <hr size="3rem" class="margin-bottom-md line-fill">

          <v-layout row margin-bottom-xl>
            <v-flex sm12 xs10 offset-xs1 >
                  <h1 class="sherpa-blue heading-small shadow-yellow margin-bottom-sm" align="left">TIMELINE KEGIATAN</h1>
                  <!-- <svg class="dash-height dash-fill margin-bottom-xs">
                    <rect width="20%" height="100%"/>
                  </svg> -->
                  <v-layout row class="dash-size line-fill margin-bottom-sm">
                  </v-layout>
                  <p class="text-xs-center">
                    <Timeline />
                  </p>
            </v-flex>
          </v-layout>
          <hr size="3rem" class="margin-bottom-md line-fill">

          <v-layout row margin-bottom-xl>
            <v-flex sm12 xs10 offset-xs1 >
                  <h1 class="sherpa-blue heading-small shadow-yellow margin-bottom-sm" align="right">HADIAH PEMENANG</h1>
                  <v-layout row right-position>
                    <svg class="dash-height dash-fill margin-bottom-xs">
                      <rect width="20%" height="100%"/>
                    </svg>
                  </v-layout>
                  <p class="sherpa-blue heading-xlarge line-height-small margin-bottom-none">RpX.000.000,-</p>
                  <p class="text-stroke heading-medium">First Prize</p>

            </v-flex>
          </v-layout>
          <hr size="3rem" class="margin-bottom-md line-fill">

          <v-layout row>
            <v-flex sm12 xs10 offset-xs1 >
                  <h1 class="sherpa-blue heading-xsmall shadow-yellow" align="left">FREQUENTLY ASKED </h1>
                  <h1 class="sherpa-blue heading-large shadow-yellow margin-bottom-sm" align="left">QUESTIONS</h1>
                  <v-layout row class="dash-size line-fill margin-bottom-sm">
                  </v-layout>
                  <p class="text-xs">
                    <Accordion headerMsg="Sistem lombanya seperti apa?" contentMsg="Kaya gini nih!" />
                    <Accordion headerMsg="Sistem lombanya seperti apa?" contentMsg="Kaya gini nih!" />
                    <Accordion headerMsg="Sistem lombanya seperti apa?" contentMsg="Kaya gini nih!" />
                    <Accordion headerMsg="Sistem lombanya seperti apa?" contentMsg="Kaya gini nih!" />
                    <Accordion headerMsg="Sistem lombanya seperti apa?" contentMsg="Kaya gini nih!" />
                  </p>
            </v-flex>
          </v-layout>
        </v-container>
      </v-responsive>
    </v-slide-y-transition>
  </v-container>
</template>

<script>
import Accordion from '../partials/Accordion'
import Timeline from '../partials/Timeline'
export default {
  name: 'Technovation',
  components: {
    Accordion, 
    Timeline
  },
  props: {
    msg: String
  }
}
</script>

<style scoped>
  .sherpa-blue {
    color: #04464F;
  }
  .shadow-yellow {
    text-shadow: -4px 4px #FFFF00;
  }
  .text-stroke {
    -webkit-text-stroke-color: #04464F !important;
    -webkit-text-stroke-width: 0.1rem;
    color: transparent;
  }
  .box-stroke {
    background-color: transparent !important;
    border: #04464F solid !important;
  }
  .heading-xlarge {
    letter-spacing: normal!important; 
    font-size: 5rem;
  }
  .heading-large {
    letter-spacing: normal!important;
    font-size: 3.5rem;
  }
  .heading-medium {
    font-size: 3rem;
  }
  .heading-small {
    font-size: 2.5rem;
  }
  .heading-xsmall {
    font-size: 2rem;
  }
  .content-text {
    font-size: 1.5rem;
  }
  .line-height-small {
    line-height: 1;
  }
  .dash-box {
    display: inline-block;
    -webkit-transform: scale(2,1);
    -moz-transform: scale(2,1);
    -ms-transform: scale(2,1);
    -o-transform: scale(2,1);
    transform: scale(2,1);
    margin-left: 1rem;
  }
  .margin-bottom-xl {
    margin-bottom: 8rem;
  }
  .margin-bottom-md {
    margin-bottom: 4rem;
  }
    .margin-bottom-sm {
    margin-bottom: 2rem;
  }
  .margin-bottom-xs {
    margin-bottom: 1rem;
  }
  .margin-bottom-none {
    margin-bottom: 0px;
  }
  .dash-height {
    height: 0.5rem;
    overflow: hidden;
  }
  .dash-size {
    width: 5rem;
    height: 0.5rem;
  }
  .dash-fill {
    fill: #04464F;
  }
  .line-fill {
    color: #04464F;
    background-color: #04464F;
  }
  .right-position {
    -webkit-transform: scale(-1,1);
    -moz-transform: scale(-1,1);
    -ms-transform: scale(-1,1);
    -o-transform: scale(-1,1);
    transform: scale(-1,1);
  }
</style>