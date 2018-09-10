<template>
  <v-toolbar fixed light color="transparent" flat>
    <v-toolbar-title class="primary--text">
        <router-link to="/" style="text-decoration: none;">
            <v-layout>
                <img src="https://static.arkavidia.id/5/images/logo.svg" alt="" height="40">
                <h1 class="futura-bt bold" style="margin-left: 10px; text-decoration: none !important;">
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
    <toolbar-link title="Login" href="https://app.arkavidia.id/login"/>
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
      {title: "Seminar", to: "/event/seminar"},
      {title: "IT Festival", to: "/event/festival"}
    ],
    competitions: [
      {title: "Technovation", to: "/competition/technovation"},
      {title: "Programming Contest", to: "/competition/cp"},
      {title: "Capture the Flag", to: "/competition/ctf"},
      {title: "Arkalogica", to: "/competition/arkalogica"}
    ]
  })
}
</script>
<style scoped>
  * {
    font-family: 'Futura Md BT'
  }
</style>

