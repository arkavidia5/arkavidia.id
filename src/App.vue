<template>
  <v-app class="secondary">
    <Toolbar/>
    <v-content>
      <router-view></router-view>
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
    Home,
    Toolbar,
    Footer,
  }
}

</script>

<style>
  .futura-bt {
    font-family: 'Futura Md BT Bold'
  }
  .no-decoration {
    text-decoration: none !important;
  }
</style>
