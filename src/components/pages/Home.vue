<template>
  <v-container fluid no-padding>
    <v-layout row section landing >
      <v-responsive :aspect-ratio="19/9">
        <h1 class="futura-lt bold" style="font-size:3vw;position:absolute;bottom: 36%; left: 10%;">
          Awakening Future Generation's Potential
        </h1>
        <h1 class="futura-lt bold" style="font-size:5vw;bottom:24%;left:10%;position:absolute">
          Through IT
        </h1>
      </v-responsive>
    </v-layout>
    <v-layout row gradient down>
    
    </v-layout>

    <v-layout row gradient up>

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
.gradient.down {
  background: linear-gradient(to bottom,#04464F,#04464F,transparent);
  height: 80px;
  margin-top:-1px;
}
.gradient.up{
  background: linear-gradient(to bottom,transparent,#04464F,#04464f);
  height: 80px;
  margin-top:-1px;
}
</style>
