<template>
 <div >
     <v-toolbar color="primary" dark fixed app flat>
        <v-toolbar-title>
          <router-link to="/" style="text-decoration: none; color: #FFFFFF;">
            <v-layout row align-center >
              <img src="https://static.arkavidia.id/5/images/logo.svg" alt="" height="30px">
              <v-layout ml-1 futura-bt bold>
                  ARKAVIDIA 5.0
              </v-layout>
            </v-layout>
          </router-link>
        </v-toolbar-title>
        <v-spacer></v-spacer>
        <v-toolbar-side-icon @click.stop="drawer = !drawer"></v-toolbar-side-icon>
    </v-toolbar>
    <v-navigation-drawer app v-model="drawer" disable-resize-watcher>
      <v-list>
      <DrawerListItem to="/"  title="Home" active/>
      <DrawerListGroup title="Pre-Events" :items=preevents />
      <DrawerListGroup title="Events" :items=events />
      <DrawerListGroup title="Competitions" :items=competitions />
      <DrawerListItem to="/about" title="About"/>
      <a href="https://dashboard.arkavidia.id/" target="_blank" class="no-decoration">
            <v-list-tile>
                <v-list-tile-content>
                <v-list-tile-title>Login</v-list-tile-title>
                </v-list-tile-content>
            </v-list-tile>
      </a>  
      </v-list>
  </v-navigation-drawer>
 </div>
</template>

<script>
  import DrawerListItem from './Drawer/DrawerListItem'
  import DrawerListGroup from './Drawer/DrawerListGroup'
  export default {
    name: 'NavigationDrawer',
    components: {
      DrawerListItem,
      DrawerListGroup
    },
    data () {
      return {
        drawer: false,
        right: null,
        preevents: [
            {title: "Global Game Jam", to: "/preevent/gamejam"},
            {title: "Coding Class", to: "/preevent/codingclass"}
        ],
        events: [
            {title: "ArkavTalk", to: "/event/arkavtalk"},
            {title: "IT Festival", to: "/event/festival"}
        ],
        competitions: [
          {title: "Technovation", to: "/competition/technovation"},
          {title: "Competitive Programming", to: "/competition/cp"},
          {title: "Capture the Flag", to: "/competition/ctf"},
          {title: "Arkalogica", to: "/competition/arkalogica"}
        ]
      }
    }
  }
</script>
