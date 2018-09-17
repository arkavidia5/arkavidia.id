<template>
  <v-container fluid no-padding>
  <v-layout row gradient up/>
  <v-footer color="primary" dark style="height: unset">
    
    <v-container fluid style="padding:15px 3% 0 3%;" mb-2 >
      
      <v-layout row social white--text primary justify-center="">
      <v-container>
        <v-layout row justify-center="">
          <h2>
            Visit our Social Media
          </h2>
        </v-layout>
        <v-layout row justify-center mt-3>
            <a href="https://www.facebook.com/arkavidia/" target="_" class="no-decoration ml-1 mr-1">
              <img src="https://static.arkavidia.id/5/images/social/white/fb-01.svg" alt="" height="30">
            </a>
            <a href="https://www.twitter.com/arkavidia_/" target="_" class="no-decoration ml-1 mr-1">
              <img src="https://static.arkavidia.id/5/images/social/white/twitter-01.svg" alt="" height="30">
            </a>
            <a href="https://www.instagram.com/arkavidia/" target="_" class="no-decoration ml-1 mr-1">
              <img src="https://static.arkavidia.id/5/images/social/white/insta-01.svg" alt="" height="30">
            </a>
        </v-layout>
      </v-container>
    </v-layout>
    
    <!-- <v-layout primary row white--text >
      <v-container>
        <v-layout row wrap>
          <v-flex md4 xs12 box-wrapper>
            <h3 class="futura-lt bold">Sponsors</h3>
            <v-flex white sponsor-box mt-2>

            </v-flex>
          </v-flex>
          <v-flex md8 xs12 p-3 box-wrapper>
            <h3 class="futura-lt bold">
              Media Partners
            </h3>
            <v-flex white medpar-box mt-2>

            </v-flex>
          </v-flex>
        </v-layout>
      </v-container>
    </v-layout> -->
      <v-layout row class="horizontal-line">
      </v-layout>
      <v-layout row wrap>
        <v-flex md4 style="font-size: 1rem; text-align:center" >
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
          <router-link class="white--text no-decoration" to="/faq">FAQ</router-link>
          <router-link class="white--text no-decoration" to="/contact">Contact Us</router-link>
          </v-layout>
        </v-flex>
      </v-layout>
    </v-container>
  </v-footer>
  </v-container>
</template>

<script>
export default {
  name: 'Footer'
  
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
  .sponsor-box, .medpar-box {
    width: 100%;
    height: 300px;
  }
  .box-wrapper {
    padding: 15px;
  }
</style>


