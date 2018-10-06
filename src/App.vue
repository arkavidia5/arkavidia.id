<template>
  <v-app class="secondary" id="main-app-wrapper">
    <Toolbar v-if="this.$vuetify.breakpoint.mdAndUp"/>
    <NavigationDrawer v-else/>
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
// import CP from './components/pages/CP.vue'
// import CTF from './components/pages/CTF.vue'
import FAQ from './components/pages/FAQ.vue'
// import Festival from './components/pages/Festival.vue'
import Technovation from './components/pages/Technovation.vue'
// import Arkalogica from './components/pages/Arkalogica.vue';
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
  // {path: "/competition/cp", component: CP},
  // {path: "/competition/ctf", component: CTF},
  {path: "/competition/technovation", component: Technovation},
  // {path: "/competition/arkalogica", component: Arkalogica},
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
</style>
