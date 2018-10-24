<template>
  <v-app class="secondary" id="main-app-wrapper">
    <Toolbar v-if="this.$vuetify.breakpoint.mdAndUp" class="front"/>
    <NavigationDrawer v-else class="front"/>
    <v-content style="margin-top: 40px;">
      <transition name="fade">
        <router-view></router-view>
      </transition>
    </v-content>

    <Footer/> 
  </v-app>
</template>

<script>
import $ from 'jquery'
import Home from './components/pages/Home.vue'
import About from './components/pages/About.vue'
// import Contact from './components/pages/Contact.vue'
import CP from './components/pages/CP.vue'
import CTF from './components/pages/CTF.vue'
import FAQ from './components/pages/FAQ.vue'
// import Festival from './components/pages/Festival.vue'
import Technovation from './components/pages/Technovation.vue'
import Arkalogica from './components/pages/Arkalogica.vue';
// import Seminar from './components/pages/Seminar.vue';

import Toolbar from './components/partials/Toolbar.vue'
import Footer from './components/partials/Footer.vue'
import NavigationDrawer from './components/partials/NavigationDrawer.vue'
import VueRouter from 'vue-router'

const routes = [
  {path: "/", component: Home},
  {path: "/about", component: About},
  {path: "/faq", component: FAQ},
  // {path: "/contact", component: Contact},
  {path: "/competition/cp", component: CP},
  {path: "/competition/ctf", component: CTF},
  {path: "/competition/technovation", component: Technovation},
  {path: "/competition/arkalogica", component: Arkalogica},
  // {path: "/event/festival", component: Festival},
  // {path: "/event/seminar", component: Seminar}, 
]

const router = new VueRouter({
  routes: routes,
  mode: 'history',
});

export default {
  name: 'App',
  router,
  components: {
    Toolbar,
    Footer,
    NavigationDrawer
  },
  methods: {
    checkRoute(path) {
      if(path.includes("competition")) {
       $('.v-content').addClass('competition');
      } else {
        $('.v-content').removeClass('competition');
      }
    }
  },
  mounted: function(){
    this.checkRoute(window.location.pathname)
  },
  watch: {
    $route (to){
      this.checkRoute(to.path);
    }
  }
 
}

</script>

<style>
  .front {
    z-index: 99999;
  }
  .v-content.competition {
    background-image: url('./assets/bg_pattern.png') !important;
    background-size: 80%;
    background-position: top left;
    background-repeat: repeat;
  }
  .futura-bt {
    font-family: 'Futura Md BT Bold'
  }
  .futura-bt.bold {
    font-family: 'Futura Md BT Bold';
  }
  .futura-lt.bold {
    font-family: 'FuturaLT'
  }
  .futura-lt.bold {
    font-family: 'FuturaLT-Bold'
  }
  * {
    font-family: 'Futura Md BT';
  }

  .no-decoration {
    text-decoration: none !important;
  }
  .full-page {
    height: 100vh;
  }
  .no-padding {
    padding: 0;
  }
  .fade-enter-active, .fade-leave-active {
    transition-property: opacity;
    transition-duration: .25s;
  }

  .fade-enter-active {
    transition-delay: .25s;
  }

  .fade-enter, .fade-leave-active {
    opacity: 0;
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
    margin-bottom: -1px;
  }
  .heading {
    font-size: 2rem;
    color: #04464F;
  }
  .flex-column {
    flex-direction: column;
  }
  .sherpa-blue {
    color: #04464F;
  }
  .shadow-yellow {
    text-shadow: -4px -4px #FFFF00;
  }
  .text-stroke {
    -webkit-text-stroke-color: #04464F !important;
    -webkit-text-stroke-width: 0.1rem;
    color: transparent;
  }
  .box-stroke {
    background-color: #fdfcc2 !important;
    border: 0.3rem #04464F solid !important;
    box-shadow: 0.2rem 0.25rem rgba(0, 0, 0, 0.3) !important;
    font-weight: bold !important;
    font-size: 1.1rem;
  }
  .text-center {
    text-align: center;
  }
  @media only screen and (max-width: 767px) {
    .heading-xlarge {
    letter-spacing: normal!important; 
    font-size: 3.2rem;
    }
    .heading-large {
      letter-spacing: normal!important;
      font-size: 2.5rem;
    }
    .heading-medium {
      font-size: 2rem;
    }
    .heading-small {
      font-size: 1.5rem;
    }
    .heading-xsmall {
      font-size: 1rem;
    }
     .margin-bottom-xl {
      margin-bottom: 4rem;
    }
    .margin-bottom-md {
      margin-bottom: 2rem;
    }
    .margin-bottom-sm {
    margin-bottom: 1rem;
    }
    .margin-bottom-xs {
      margin-bottom: .5rem;
    }
    .margin-bottom-none {
      margin-bottom: 0px;
    }
    .content-text {
      font-size: 1.3rem;
      text-align: center;
    }
  }
  @media only screen and (min-width: 768px) {
    .heading-xlarge {
      letter-spacing: normal!important; 
      font-size: 5rem;
    }
    .heading-large {
      letter-spacing: normal!important;
      font-size: 3.5rem;
    }
    .heading-medium {
      font-size: 3rem;
    }
    .heading-small {
      font-size: 2.5rem;
    }
    .heading-xsmall {
      font-size: 2rem;
    }
    .margin-bottom-xl {
    margin-bottom: 8rem;
    }
    .margin-bottom-md {
      margin-bottom: 4rem;
    }
      .margin-bottom-sm {
      margin-bottom: 2rem;
    }
    .margin-bottom-xs {
      margin-bottom: 1rem;
    }
    .margin-bottom-none {
      margin-bottom: 0px;
    }
    .content-text {
      font-size: 1.5rem;
    }
    .text-md-center {
      text-align: center;
    }
    .text-md-left {
      text-align: left;
    }
    .text-md-right {
      text-align: right; 
    }
    .justify-md-start {
      justify-content: start;
    }
    .ml-md-4 {
      margin-left: 15px;
    }
    .ml-md-1 {
      margin-left: 10px;
    }
    .ml-md-0 {
      margin-left: 0;
    }
  }
 
  .line-height-small {
    line-height: 1;
  }
  .dash-box {
    display: inline-block;
    -webkit-transform: scale(2,1);
    -moz-transform: scale(2,1);
    -ms-transform: scale(2,1);
    -o-transform: scale(2,1);
    transform: scale(2,1);
    margin-left: 1rem;
  }
  
  .dash-height {
    height: 0.5rem;
    overflow: hidden;
  }
  .dash-size {
    width: 5rem;
    height: 0.5rem;
  }
  .dash-fill {
    fill: #04464F;
  }
  .line-fill {
    color: #04464F;
    background-color: #04464F;
  }
  .right-position {
    -webkit-transform: scale(-1,1);
    -moz-transform: scale(-1,1);
    -ms-transform: scale(-1,1);
    -o-transform: scale(-1,1);
    transform: scale(-1,1);
  }
</style>
