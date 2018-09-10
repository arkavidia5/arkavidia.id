<template>
  <v-footer color="primary" dark height="60">
    <v-container fluid style="padding:15px 3% 0 3%;" mb-2 >
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
 
</style>


