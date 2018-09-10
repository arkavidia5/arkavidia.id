<template>
  <v-container fluid no-padding>
    <v-layout row section landing>
      <v-responsive :aspect-ratio="18/9" class="primary--text">
        <h1 class="futura-lt bold" style="font-size:3.2vw;position:absolute;bottom: 34.5%; left: 10%;">
          Awakening Future Generation's Potential
        </h1>
        <h1 class="futura-lt bold" style="font-size:4.6vw;bottom:24%;left:10%;position:absolute">
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
    <PageBreak/>
     <v-layout row section events justify-center>
      <h1 class="futura-lt bold heading">
        Events
      </h1>
    </v-layout>
    <PageBreak/>
     <v-layout row section competitions justify-center>
      <h1 class="futura-lt bold heading">
        Competitions
      </h1>
    </v-layout>
    <PageBreak/>
     <v-layout row section schedule justify-center>
      <h1 class="futura-lt bold heading">
        Schedule
      </h1>
    </v-layout>
    <v-layout row gradient up/>
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
    <v-layout primary row white--text >
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
    </v-layout>
  </v-container>
</template>

<script>
import PageBreak from '@/components/partials/PageBreak'
export default {
  name: 'Home',
  components: {
    PageBreak
  },
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
  font-size: 52sp;
  color: #04464F;
}

.sponsor-box, .medpar-box {
  width: 100%;
  height: 300px;
}
.box-wrapper {
  padding: 15px;
}
</style>
