<template>
  <v-app class="secondary">
    <Toolbar/>
    <v-content style="padding-top: 55px;">
      <transition name="fade">
        <router-view></router-view>
      </transition>
    </v-content>
    <Footer/> 
  </v-app>
</template>

<script>
import Home from './components/pages/Home.vue'
import About from './components/pages/About.vue'
import Toolbar from './components/partials/Toolbar.vue'
import Footer from './components/partials/Footer.vue'
import VueRouter from 'vue-router'
const routes = [
  {path: "/", component: Home},
  {path: "/about", component: About}
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
  }
}

</script>

<style>
  .futura-bt {
    font-family: 'Futura Md BT Bold'
  }
  * {
    font-family: 'Futura Md BT';
  }
  .bold {
    font-family: 'Futura Md BT Bold';
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
</style>
