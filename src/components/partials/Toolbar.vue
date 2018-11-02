<template>
  <v-toolbar fixed v-bind:light="this.backgroundStyle.opacity < 0.8 && !toolbarForceWhite" v-bind:dark="this.backgroundStyle.opacity >= 0.8 || toolbarForceWhite" color="transparent" flat v-scroll="onScroll">
    <v-layout class="background" primary v-bind:style="backgroundStyle">
      &nbsp;
    </v-layout>
    <v-toolbar-title>
        <router-link to="/" style="text-decoration: none;">
            <v-layout>
                <img src="https://static.arkavidia.id/5/images/logo.svg" alt="" height="40">
                <h1 class="futura-bt bold" v-bind:class="{'white--text': backgroundStyle.opacity >=0.8 || toolbarForceWhite}" style="margin-left: 10px; text-decoration: none !important;">
                    ARKAVIDIA 5.0
                </h1>
            </v-layout>
        </router-link>
    </v-toolbar-title>
    <v-spacer></v-spacer>
    <toolbar-link title="Home" to="/"/>
    <toolbar-dropdown title="Events" :items=events />
    <toolbar-dropdown title="Competitions" :items=competitions /> 
    <toolbar-link title="About" to="/about" />
    <!-- <toolbar-link title="Login" href="https://app.arkavidia.id/login"/> -->
  </v-toolbar>
</template>
<script>
import ToolbarDropdown from './Toolbar/ToolbarDropdown'
import ToolbarLink from './Toolbar/ToolbarLink'
export default {
  name: 'Toolbar',
  components: {
      'toolbar-dropdown': ToolbarDropdown,
      'toolbar-link': ToolbarLink
  },
  data: () => ({
    events: [
      {title: "ArkavTalk", to: "/event/arkavtalk"},
      {title: "IT Festival", to: "/event/festival"}
    ],
    competitions: [
      {title: "Technovation", to: "/competition/technovation"},
      {title: "Competitive Programming", to: "/competition/cp"},
      {title: "Capture the Flag", to: "/competition/ctf"},
      {title: "Arkalogica", to: "/competition/arkalogica"}
    ],
    offsetTop: 0,
    toolbarForceWhite: false,
    backgroundStyle: {
      opacity:0,
    }
  }),
  methods: {
    onScroll () {
      this.offsetTop = window.pageYOffset || document.documentElement.scrollTop;
      this.backgroundStyle.opacity = this.offsetTop == 0 ? 0 : 1;
    }
  }
}
</script>
<style scoped>
  * {
    font-family: 'Futura Md BT'
  }
  .background {
    position: absolute;
    height: 100%;
    width: 100%;
    left:0;
    top:0;
    z-index: -100;
    transition: 0.5s ease-in-out;
  }
  
</style>

