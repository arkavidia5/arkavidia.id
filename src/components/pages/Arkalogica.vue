<template>
  <v-container fluid>
    <v-slide-y-transition mode="out-in">
        <v-container no-padding>
          <v-layout row margin-bottom-xl>
            <v-flex sm12 xs12 md8>
              <v-layout class="row">
                    <v-flex md12 xs8 style="z-index: 2">
                      <p class="text-stroke heading-medium line-height-small margin-bottom-none">Competition 
                        <span class="dash-box">_</span>
                      </p>
                      <h1 class="sherpa-blue heading-large shadow-yellow margin-bottom-sm" align="left">ARKALOGICA</h1>
                    </v-flex>
                    <v-flex xs4 style="z-index: 1" v-if="this.$vuetify.breakpoint.smAndDown">
                      <img src="../../assets/tower_logica.svg" alt="technovation-ico" height="150px" style="margin-top: -50px; margin-left: 20px;">
                    </v-flex>
                  </v-layout>
                  <v-layout row>
                    <v-flex class="d-flex flex-column">
                      <p class="content-text margin-bottom-xs">
                        Arkalogica adalah singkatan dari Arkavidia Logic Competition. Melalui kegiatan ini diharapkan terciptanya generasi yang hebat dalam berpikir logis dan analitis dan juga meningkatkan kerjasama antar peserta.
                      </p>
                      <h2 class="heading heading-small text-left">
                        Kategori Peserta
                      </h2>
                      <v-layout row mb-4  justify-start>
                        <v-flex align-center xs3 d-flex ml-md-4>
                          <img src="https://static.arkavidia.id/5/images/icons/siswa.svg" alt="mahasiswa" height="50"> 
                          <span style="font-size: 1.1rem; margin-left: 10px;">Siswa SMA/Sederajat</span>
                        </v-flex>
                      </v-layout>
                      <v-layout row class="dash-size line-fill margin-bottom-sm justify-center justify-md-start ml-auto mr-auto ml-md-0">
                      </v-layout>
                      <!-- <v-layout row justify-center justify-md-start>
                        <a href="https://static.arkavidia.id/5/rulebook/Arkavidia5_Arkalogica_Rulebook.pdf" class="no-decoration" target="_blank">
                          <v-btn class="box-stroke">Unduh Rulebook
                          </v-btn>
                        </a>
                        <v-btn class="box-stroke">Daftar Sekarang!
                        </v-btn>
                      </v-layout> -->

                    </v-flex>
                  
                  </v-layout>
            </v-flex>
            <v-flex md4 xs4 class="d-flex flex-column " v-if="this.$vuetify.breakpoint.mdAndUp"> 
              <img src="../../assets/tower_logica.svg" alt="technovation-ico" height="250px">
            </v-flex>
          </v-layout>
          <hr size="3rem" class="margin-bottom-md line-fill">

          <v-layout row margin-bottom-xl>
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
          <hr size="3rem" class="margin-bottom-md line-fill">

          <v-layout row margin-bottom-xl justify-center>
            <v-flex sm12 xs12>

            <!-- <v-flex sm12 xs10 offset-xs1 >
                  <h1 class="sherpa-blue heading-small shadow-yellow margin-bottom-sm" align="right">HADIAH PEMENANG</h1>
                  <v-layout row right-position>
                    <svg class="dash-height dash-fill margin-bottom-xs">
                      <rect width="20%" height="100%"/>
                    </svg>
                  </v-layout>
                  <p class="sherpa-blue heading-xlarge line-height-small margin-bottom-none">Rp4.500.000,-</p>
                  <p class="text-stroke heading-medium">Total Prize</p>

            </v-flex> -->
                <v-flex md11 sm11>
                  <h1 class="sherpa-blue heading-small shadow-yellow margin-bottom-sm" align="right">HADIAH PEMENANG</h1>
                  <v-layout row right-position>
                    <svg class="dash-height dash-fill margin-bottom-xs">
                      <rect width="20%" height="100%"/>
                    </svg>
                  </v-layout>
                </v-flex>
                  <!-- <p class="sherpa-blue heading-xlarge line-height-small margin-bottom-none">Rp16.750.000,-</p>
                  <p class="text-stroke heading-medium">Total Prize</p> -->
                <v-layout row>
                  <v-flex md12 xs12>
                    <p class="sherpa-blue heading-xlarge line-height-small margin-bottom-none" align="center">Rp4.500.000,-</p>
                    <p class="text-stroke heading-medium" align="center">Total Prize</p>
                  </v-flex>
                </v-layout>

                  <v-layout>
                    <v-flex md12 xs12>
                      <p class="text-stroke heading-small margin-bottom-none" align="center">Juara 1</p>
                      <p class="sherpa-blue heading-small line-height-small" align="center">Rp2.000.000,-</p>
                      <p class="text-stroke heading-small margin-bottom-none" align="center">Juara 2</p>
                      <p class="sherpa-blue heading-small line-height-small" align="center">Rp1.500.000,-</p>
                      <p class="text-stroke heading-small margin-bottom-none" align="center">Juara 3</p>
                      <p class="sherpa-blue heading-small line-height-small" align="center">Rp1.000.000,-</p>
                    </v-flex>
                  </v-layout>
                </v-flex>

          </v-layout>
          <hr size="3rem" class="margin-bottom-md line-fill">

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
  name: 'Arkalogica',
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
  
</style>
