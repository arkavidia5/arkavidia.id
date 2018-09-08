<template>
  <v-app class="secondary">
    <Toolbar/>
    <v-content>
      <router-view></router-view>
    </v-content>
  </v-app>
</template>

<script>
import Home from './components/pages/Home.vue'
import About from './components/pages/About.vue'
import Toolbar from './components/partials/Toolbar.vue'

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
  }
}

</script>

<style>
  .futura-bt {
    font-family: 'Futura Md BT'
  }
</style>
