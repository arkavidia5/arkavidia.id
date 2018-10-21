<template>
  <v-container fluid>
    <v-slide-y-transition mode="out-in">
      <v-responsive :aspect-ratio="1.60 " class="row technovation-background">
        <v-container>
          <v-layout row margin-bottom-xl>
            <v-flex sm12 xs10 md8>
                  <p class="text-stroke heading-medium line-height-small margin-bottom-none">Competition 
                    <span class="dash-box">_</span>
                  </p>
                  <h1 class="sherpa-blue heading-large shadow-yellow margin-bottom-sm" align="left">TECHNOVATION</h1>
                  <v-layout row>
                    <v-flex class="d-flex flex-column">
                      <p class="content-text margin-bottom-xs">
                        Lomba Technovation merupakan lomba pengembangan ide perangkat lunak yang dapat diikuti oleh setiap mahasiswa-mahasiswi di Indonesia. Titik berat pada lomba ini adalah ide yang inovatif, feasible, sustainable, dan seberapa besar manfaat yang diberikan untuk kemajuan Indonesia, terutama di bidang IT.
                      </p>
                      <v-layout row class="dash-size line-fill margin-bottom-sm">
                      </v-layout>
                      <v-layout row>
                        <a href="https://static.arkavidia.id/5/rulebook/Arkavidia5_Technovation_Rulebook_v20181020.pdf" class="no-decoration" target="_blank">
                          <v-btn class="box-stroke">Unduh Rulebook
                          </v-btn>
                        </a>
                        <!-- <v-btn class="box-stroke">Daftar Sekarang!
                        </v-btn> -->
                      </v-layout>

                    </v-flex>
                  
                  </v-layout>
            </v-flex>
            <v-flex md4 xs4 class="d-flex flex-column ">
              <img src="../../assets/tower.svg" alt="technovation-ico" height="250px">
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
                    <TimelineItem direction="right" image="https://static.arkavidia.id/5/images/icons/competition/icon_pendaftaran.svg" title="PENDAFTARAN" time="29 Oktober - 25 November 2018" description="Pendaftaran dilakukan secara online melalui website"/>
                    <TimelineItem direction="left" image="https://static.arkavidia.id/5/images/icons/competition/icon_penyisihan.svg" title="PROPOSAL SUBMISSION" time="12 November 2018 - 3 Desember 2019" description="Penyisihan dilakukan secara online"/> 
                    <TimelineItem direction="right" image="https://static.arkavidia.id/5/images/icons/competition/icon_pengumuman.svg" title="PENGUMUMAN FINALIS" time="20 Januari 2019" description="Pengumuman finalis di media sosial Arkavidia 5.0"/> 
                    <TimelineItem direction="left" image="https://static.arkavidia.id/5/images/icons/competition/icon_final.svg" title="FINAL" time="10 Februari 2019" description="Final dilakukan onsite di ITB"/> 
                  </Timeline>
              </v-layout>    
            </v-flex>
            
          </v-layout>
          <hr size="3rem" class="margin-bottom-md line-fill">

          <v-layout row margin-bottom-xl>
            <v-flex sm12 xs10>
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
                <v-layout>
                  <v-flex md12 xs12>
                    <p class="sherpa-blue heading-xlarge line-height-small margin-bottom-none" align="center">Rp16.750.000,-</p>
                    <p class="text-stroke heading-medium" align="center">Total Prize</p>
                  </v-flex>
                </v-layout>

                  <v-layout>
                    <v-flex md12 xs12>
                      <p class="text-stroke heading-small margin-bottom-none" align="center">Juara 1</p>
                      <p class="sherpa-blue heading-small line-height-small" align="center">Rp7.000.000,-</p>
                      <p class="text-stroke heading-small margin-bottom-none" align="center">Juara 2</p>
                      <p class="sherpa-blue heading-small line-height-small" align="center">Rp5.000.000,-</p>
                      <p class="text-stroke heading-small margin-bottom-none" align="center">Juara 3</p>
                      <p class="sherpa-blue heading-small line-height-small" align="center">Rp3.000.000,-</p>
                      <p class="text-stroke heading-small margin-bottom-none" align="center">Juara Favorit</p>
                      <p class="sherpa-blue heading-small line-height-small" align="center">Rp1.000.000,-</p>
                      <p class="text-stroke heading-small margin-bottom-none" align="center">Best Presentation</p>
                      <p class="sherpa-blue heading-small line-height-small" align="center">Rp750.000,-</p>
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
      </v-responsive>
    </v-slide-y-transition>
  </v-container>
</template>

<script>
import Accordion from '../partials/Accordion'
import Timeline from '../partials/Timeline'
import TimelineItem from '../partials/TimelineItem'
export default {
  name: 'Technovation',
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
