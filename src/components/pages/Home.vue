<template>
  <v-container fluid no-padding>
    <v-layout row section landing >
      <v-responsive :aspect-ratio="19/9">
        <h1 class="futura-lt bold" style="font-size:3vw;position:absolute;bottom: 37%; left: 10%;">
          Awakening Future Generation's Potential
        </h1>
        <h1 class="futura-lt bold" style="font-size:5vw;bottom:25%;left:10%;position:absolute">
          Through IT
        </h1>
      </v-responsive>
    </v-layout>
  </v-container>
</template>

<script>
export default {
  name: 'Home',
  props: {
    msg: String
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
.landing {
  width: 100%;
  position: relative;  
}
.landing>div{
   background-image: url('https://static.arkavidia.id/5/images/landing-bg-2.svg');
  background-size: 102%;
  background-position: bottom;
}
</style>
