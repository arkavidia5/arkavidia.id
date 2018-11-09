<template>
  <v-container fluid>
    <v-slide-y-transition mode="out-in">
      <v-container no-padding>
        <!-- Hero -->
        <v-layout row margin-bottom-xl class="page-full page-margin" style="margin-top: -30px">
          <v-flex sm12 xs12 md12 id="comp-title">
            <div>
              <v-layout class="row">
                <v-flex md12 xs8 style="z-index: 2">
                  <p class="text-stroke heading-medium line-height-small margin-bottom-none"> 
                    Competition <span class="dash-box">_</span>
                  </p>
                  <br>
                  <h1 class="sherpa-blue heading-large shadow-yellow margin-bottom-sm" align="left">COMPETITIVE<br>PROGRAMMING</h1>
                </v-flex>
                <v-flex xs4 style="z-index: 1" id="comp-tower" v-if="this.$vuetify.breakpoint.smAndDown">
                  <img src="../../assets/tower_cp.svg" alt="technovation-ico" height="150px" style="margin-top: 0px; margin-left: 20px;">
                </v-flex>
              </v-layout>
              <v-layout row id="comp-intro">
                <v-flex class="d-flex flex-column">
                  <p class="content-text margin-bottom-xs" style="text-align:justify">
                    Kompetisi ini bertujuan untuk menguji kemampuan berpikir logis dan komputasional. Peserta akan dituntut untuk menggunakan algoritma atau struktur data yang tepat untuk menyelesaikan setiap persoalan. Ketepatan dan kecepatan dalam menyelesaikan persoalan merupakan kunci dalam kompetisi ini.
                  </p>
                  <h2 class="heading heading-small text-left">Kategori Peserta</h2>
                  <br>
                  <v-layout row mb-4 wrap justify-start>
                    <v-flex align-center xs7 md6 d-flex ml-md-4>
                      <img src="https://static.arkavidia.id/5/images/icons/mahasiswa.svg" alt="mahasiswa" height="50"> 
                      <span style="font-size: 1.1rem;" class="ml-md-1">Mahasiswa</span>
                    </v-flex>
                    <v-flex align-center xs5 md5 justify-center d-flex>
                      <img src="https://static.arkavidia.id/5/images/icons/siswa.svg" alt="mahasiswa" height="50"> 
                      <span style="font-size: 1.1rem;" class="ml-md-1">Siswa SMA/Sederajat</span>
                    </v-flex>
                  </v-layout>
                  <v-layout row class="dash-size line-fill margin-bottom-sm justify-center justify-md-start ml-auto mr-auto ml-md-0"/>
                  <v-layout row wrap>
                    <v-flex xs8 sm6 md5 offset-xs2>
                    <a href="https://static.arkavidia.id/5/rulebook/Arkavidia5_CP_Rulebook.pdf" class="no-decoration" target="_blank">
                      <v-btn class="box-stroke">Unduh Rulebook
                      </v-btn>
                    </a> 
                    </v-flex >
                    <v-flex xs8 sm6 md5 offset-xs2>
                    <a href="https://dashboard.arkavidia.id/register" class="no-decoration" target="_blank">
                      <v-btn class="box-stroke">Daftar Sekarang!
                      </v-btn>
                    </a>
                    </v-flex>
                  </v-layout>
                </v-flex>
              </v-layout>
            </div>
          </v-flex>
          <v-flex md4 xs4 class="d-flex flex-column"
            v-if="this.$vuetify.breakpoint.mdAndUp"> 
            <img src="../../assets/tower_cp.svg" alt="technovation-ico" height="250px">
          </v-flex>
        </v-layout>
        <!-- /Hero -->
        <hr size="3rem" class="margin-bottom-md line-fill page-margin">
        <!-- Timeline -->
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
                <TimelineItem direction="right" image="https://static.arkavidia.id/5/images/icons/competition/icon_pendaftaran.svg" title="PENDAFTARAN" time="5 November - 18 November 2018" description="Pendaftaran dilakukan secara online melalui website"/>
                <TimelineItem direction="left" image="https://static.arkavidia.id/5/images/icons/competition/icon_type.svg" title="BABAK PENYISIHAN" time="13 Januari 2019" description="Penyisihan dilakukan secara online"/> 
                <TimelineItem direction="right" image="https://static.arkavidia.id/5/images/icons/competition/icon_pengumuman.svg" title="PENGUMUMAN FINALIS" time="20 Januari 2019" description="Pengumuman finalis di media sosial Arkavidia 5.0"/> 
                <TimelineItem direction="left" image="https://static.arkavidia.id/5/images/icons/competition/icon_podium.svg" title="FINAL" time="9 Februari 2019" description="Final dilakukan onsite di ITB"/> 
              </Timeline>
            </v-layout>    
          </v-flex>
        </v-layout>
        <!-- /Timeline -->
        <hr size="3rem" class="margin-bottom-md line-fill page-margin">
        <!-- Prize -->
        <v-layout row margin-bottom-xl justify-center class="page-margin">
          <v-flex sm12 xs12>
            <v-flex md11 sm11>
              <h1 class="sherpa-blue heading-small shadow-yellow margin-bottom-sm" align="right">HADIAH PEMENANG</h1>
              <v-layout row right-position>
                <svg class="dash-height dash-fill margin-bottom-xs">
                  <rect width="20%" height="100%"/>
                </svg>
              </v-layout>
            </v-flex>

            <v-layout row>
              <v-flex md12 xs12>
                <p class="sherpa-blue heading-xlarge line-height-small margin-bottom-none" align="center">Rp19.500.000,-</p>
                <p class="text-stroke heading-medium" align="center">Total Prize</p>
              </v-flex>
            </v-layout>

            <v-layout row v-if="this.$vuetify.breakpoint.mdAndUp">
              <v-flex md1 xs0>
              </v-flex>
              <v-flex md5 xs16>
                <p class="sherpa-blue heading-large line-height-small">Mahasiswa</p>
                <p class="text-stroke heading-small margin-bottom-none">Juara 1</p>
                <p class="sherpa-blue heading-small line-height-small">Rp7.000.000,-</p>
                <p class="text-stroke heading-small margin-bottom-none">Juara 2</p>
                <p class="sherpa-blue heading-small line-height-small">Rp5.000.000,-</p>
                <p class="text-stroke heading-small margin-bottom-none">Juara 3</p>
                <p class="sherpa-blue heading-small line-height-small">Rp3.000.000,-</p>
              </v-flex>
              <v-flex md5 xs16>
                <p class="sherpa-blue heading-large line-height-small" align="right">SMA</p>
                <p class="text-stroke heading-small margin-bottom-none" align="right">Juara 1</p>
                <p class="sherpa-blue heading-small line-height-small" align="right">Rp2.000.000,-</p>
                <p class="text-stroke heading-small margin-bottom-none" align="right">Juara 2</p>
                <p class="sherpa-blue heading-small line-height-small" align="right">Rp1.500.000,-</p>
                <p class="text-stroke heading-small margin-bottom-none" align="right">Juara 3</p>
                <p class="sherpa-blue heading-small line-height-small" align="right">Rp1.000.000,-</p>
              </v-flex>
              <v-flex md1 xs0>
              </v-flex>
            </v-layout>
            <v-container v-else>
              <v-flex md1 xs0/>
              <v-flex md5 xs16>
                <p class="sherpa-blue heading-large line-height-small">Mahasiswa</p>
                <p class="text-stroke heading-small margin-bottom-none">Juara 1</p>
                <p class="sherpa-blue heading-small line-height-small">Rp7.000.000,-</p>
                <p class="text-stroke heading-small margin-bottom-none">Juara 2</p>
                <p class="sherpa-blue heading-small line-height-small">Rp5.000.000,-</p>
                <p class="text-stroke heading-small margin-bottom-none">Juara 3</p>
                <p class="sherpa-blue heading-small line-height-small">Rp3.000.000,-</p>
              </v-flex>
              <v-flex md5 xs16>
                <p class="sherpa-blue heading-large line-height-small" align="right">SMA</p>
                <p class="text-stroke heading-small margin-bottom-none" align="right">Juara 1</p>
                <p class="sherpa-blue heading-small line-height-small" align="right">Rp2.000.000,-</p>
                <p class="text-stroke heading-small margin-bottom-none" align="right">Juara 2</p>
                <p class="sherpa-blue heading-small line-height-small" align="right">Rp1.500.000,-</p>
                <p class="text-stroke heading-small margin-bottom-none" align="right">Juara 3</p>
                <p class="sherpa-blue heading-small line-height-small" align="right">Rp1.000.000,-</p>
              </v-flex>
              <v-flex md1 xs0/>
            </v-container>
          </v-flex>
        </v-layout>

        <hr size="3rem" class="margin-bottom-md line-fill page-margin">

        <!-- <v-layout row>
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
        </v-layout> -->
      </v-container>
    </v-slide-y-transition>
  </v-container>
</template>

<script>
import Accordion from '../partials/Accordion'
import Timeline from '../partials/Timeline'
import TimelineItem from '../partials/TimelineItem'

export default {
  name: 'CP',
  components: {
    Accordion, 
    Timeline,
    TimelineItem
  },
  props: {
    msg: String
  }
}
</script>

<style scoped>

.page-full {
  height: 100vh;
}

.page-margin {
  margin-left: 15vw;
  margin-right: 15vw;
}

#comp-title {
  display: flex;
  flex-direction: column;
  justify-content: center;
}

#comp-intro {
  padding-right: 10em;
}

@media screen and (max-width: 1024px) {
  .page-margin {
    margin-left: 5vw;
    margin-right: 5vw;
  }
}

@media screen and (max-width: 768px) {
  .page-margin {
    margin-left: 3vw;
    margin-right: 3vw;
  }

  #comp-tower {
    display: none;
  }
}

@media screen and (max-width: 480px) {
  .page-margin {
    margin-left: 1vw;
    margin-right: 1vw;
  }

  .page-full {
    height: 100%;
  }

  #comp-intro {
    padding-right: 0;
  }
}

</style>
