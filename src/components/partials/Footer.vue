<template>
  <v-footer color="primary" dark height="60">
    <v-container fluid style="padding:0 3%;">
      <v-layout row class="horizontal-line">
      </v-layout>
      <v-layout row>
        <span>
          &copy;2018 -  Arkavidia 5.0 Creative and IT Developer Team
        </span>
        <v-spacer></v-spacer>
          <router-link class="white--text no-decoration" to="/about">About</router-link>
          <router-link class="white--text no-decoration" to="/faq">FAQ</router-link>
          <router-link class="white--text no-decoration" to="/contact">Contact Us</router-link>
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
    margin-left: 30px;
    margin-right: 0px;
  }
  .horizontal-line {
    background: white;
    height: 3px;
    margin-bottom: 9px;
  }
</style>


