<template>
  <v-container fluid no-padding>
    <v-layout row section landing>
      <v-responsive :aspect-ratio="18/9" class="primary--text">
        <h1 class="futura-lt bold" style="font-size:2.8vw;position:absolute;bottom: 35%; left: 10%;">
          Awakening Future Generation's Potential
        </h1>
        <h1 class="futura-lt bold" style="font-size:4.8vw;bottom:25%;left:10%;position:absolute">
          Through IT
        </h1>
      </v-responsive>
    </v-layout>
    <v-layout row gradient down/>
    <v-layout row section whats-on justify-center>
      <h1 class="futura-lt bold heading">
        What's on Arkavidia?
      </h1>
    </v-layout>
    <v-layout row gradient up/>
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
.gradient {
  height: 60px;
}
.gradient.down {
  background: linear-gradient(to bottom,#04464F,#04464F,transparent);
  margin-top:-1px;
}
.gradient.up{
  background: linear-gradient(to bottom,transparent,#04464F,#04464F);
}
.heading {
  font-size: 2.5vw;
  color: #04464F;
}

</style>
