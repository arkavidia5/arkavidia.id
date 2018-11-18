<template>
  <v-footer style="height: unset;background:transparent" dark>
    <v-container fluid no-padding>
      <!--v-layout v-if="gradientEnabled" row gradient up /-->
      <v-layout row primary>
        <v-container fluid style="padding:15px 3% 0 3%;" mb-2>
          <v-layout row social white--text primary justify-center="">
          <v-container >
            <v-layout row justify-center="">
              <h2>
                Visit our Social Media
              </h2>
            </v-layout>
            <v-layout row justify-center mt-3>
                <a href="https://www.facebook.com/arkavidia/" target="_" class="no-decoration ml-1 mr-1">
                  <img src="https://static.arkavidia.id/5/images/social/white/fb-01.svg" alt="" height="30">
                </a>
                <a href="https://www.twitter.com/arkavidia5/" target="_" class="no-decoration ml-1 mr-1">
                  <img src="https://static.arkavidia.id/5/images/social/white/twitter-01.svg" alt="" height="30">
                </a>
                <a href="https://www.instagram.com/arkavidia/" target="_" class="no-decoration ml-1 mr-1">
                  <img src="https://static.arkavidia.id/5/images/social/white/insta-01.svg" alt="" height="30">
                </a>
            </v-layout>
          </v-container>
        </v-layout>
        
        <v-layout primary row white--text >
          <v-container>
            <v-layout row wrap>
              <v-flex md5 sm6 xs12 box-wrapper>
                <h3 class="futura-lt bold">Sponsors</h3>
                <v-flex box mt-2>
                  <v-layout row wrap>
                    <v-flex v-for="item in sponsors" :key="item.name" :class="item.size == 'L' ? 'xs12' : item.size == 'M' ? 'xs6' : 'xs3'" d-flex justify-center align-center>
                      <img :src="item.url" :alt="item.name" width="100%" :class="`sp-${item.size}-logo`">
                    </v-flex>
                  </v-layout>
                </v-flex>
              </v-flex>
              <v-flex md5 sm6 xs12 p-3 box-wrapper>
                <h3 class="futura-lt bold">
                  Media Partners
                </h3>
                <v-flex box mt-2>
                  <v-layout class="row wrap">
                    <v-flex v-for="item in medpars" :key="item.name" xs4 d-flex justify-center align-center pa-1>
                      <img :src="item.url" :alt="item.name" width="100%" :class="`mp-logo`">
                    </v-flex>
                  </v-layout>
                </v-flex>
                <h3 class="futura-lt bold">
                  Community Partners
                </h3>
                <v-flex box mt-2>
                  <v-layout class="row wrap">
                    <v-flex v-for="item in compars" :key="item.name" xs4 d-flex justify-center align-center pa-1>
                      <img :src="item.url" :alt="item.name" width="100%" :class="`mp-logo`">
                    </v-flex>
                  </v-layout>
                </v-flex>
              </v-flex>
              <v-flex md2 sm6 offset-md0 offset-sm3 xs12 p-3 box-wrapper>
                <h3 class="futura-lt bold text-sm-center text-xs-left text-md-left">
                  Organized By
                </h3>
                <v-layout row wrap>
                  <v-flex xs6 md12 justify-center align-center d-flex pa-2>
                    <img src="https://static.arkavidia.id/5/logo/hmif.png" alt="" width="100%">
                  </v-flex>
                  <v-flex xs6 md12 justify-center align-center d-flex pa-2>
                    <img src="https://static.arkavidia.id/5/logo/itb.gif" alt="" width="100%">
                  </v-flex>
                </v-layout>

              </v-flex>
            </v-layout>
          </v-container>
        </v-layout>
        <v-layout row class="horizontal-line">
          </v-layout>
          <v-layout row wrap>
            <v-flex md4 xs12 style="font-size: 1rem; text-align:center" >
            <small v-if="this.$vuetify.breakpoint.smAndDown">
              &copy;2018 -  Arkavidia 5.0 Creative and IT Developer Team
            </small>
            <span v-else>
              &copy;2018 -  Arkavidia 5.0 Creative and IT Developer Team
            </span>
            
            </v-flex>
            <v-flex md8>
              <v-layout row v-bind:justify-end="this.$vuetify.breakpoint.mdAndUp" v-bind:justify-center="this.$vuetify.breakpoint.smAndDown">
              <router-link class="white--text no-decoration" to="/about">About</router-link>
              <!-- <router-link class="white--text no-decoration" to="/faq">FAQ</router-link>
              <router-link class="white--text no-decoration" to="/contact">Contact Us</router-link> -->
              </v-layout>
            </v-flex>
          </v-layout>
        </v-container>
      </v-layout>
    </v-container>
  </v-footer>
</template>

<script>
export default {
  name: 'Footer',
    data: () => ({
      gradientEnabled: true,
      sponsors: [
        {
          "name": "AWS Educate",
          "url" : "https://static.arkavidia.id/5/logo/aws.svg",                 
          "size": "M",
        },
        {
          "name": "Shopee",
          "url" : "https://static.arkavidia.id/5/logo/shopee.png",                 
          "size": "M",
        }
      ],
      medpars: [
        {
          "name": "Kampus Update",
          "url" : "https://static.arkavidia.id/5/logo/kampusupdate.png",
        },
        {
          "name": "Event Kampus",
          "url": "https://static.arkavidia.id/5/logo/eventkampus.png",
        },
        {
          "name": "Techno Event Academy",
          "url": "https://static.arkavidia.id/5/logo/technoeventacademy.jpg"
        },
        {
          "name": "Seputar Event",
          "url": "https://static.arkavidia.id/5/logo/seputarevent.png",
        }
      ],
      compars: [
        {
          "name": "Geek Hunter",
          "url" : "https://static.arkavidia.id/5/logo/geekhunter.jpg",
        }
      ]
    }),
  methods: {
      checkRoute(path) {
          if(path.includes("festival")) {
              this.gradientEnabled = false;
          } else {
              this.gradientEnabled = true;
          }
      }
  },
  watch: {
      $route (to){
          this.checkRoute(to.path);
      }
  },
  mounted: function() {
      this.checkRoute(window.location.pathname)
  }
}
</script>

<style scoped>
  * {
    font-family: 'Futura Md BT'
  }
  a {
    margin-left: 15px;
    margin-right: 15px;
  }
  .horizontal-line {
    background: white;
    height: 3px;
    margin-bottom: 9px;
  }
  .box {
    width: 100%;
  }
  .box-wrapper {
    padding: 15px;
  }
  .sp-L-logo {
    object-fit: contain;
    max-height: 120px;
  }
  .sp-M-logo {
    object-fit: contain;
    max-height: 80px;
  }
  .sp-S-logo {
      object-fit: contain;
    max-height: 60px;
  }
  .mp-logo {
    max-height: 60px;
    object-fit: contain;
  }

</style>


