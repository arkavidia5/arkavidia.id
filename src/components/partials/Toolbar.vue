<template>
  <v-toolbar light color="secondary" class="elevation-0">
    <v-toolbar-title class="primary--text">
        <router-link to="/" style="text-decoration: none;">
            <v-layout>
                <img src="https://static.arkavidia.id/5/images/logo.svg" alt="" height="40">
                <h1 class="futura-bt" style="margin-left: 10px; text-decoration: none !important;">
                    Arkavidia 5.0
                </h1>
            </v-layout>
        </router-link>
    </v-toolbar-title>
    <v-spacer></v-spacer>
    <v-btn icon>
        <v-icon>search</v-icon>
    </v-btn>
    <v-btn icon>
        <v-icon>apps</v-icon>
    </v-btn>
    <v-btn icon>
        <v-icon>refresh</v-icon>
    </v-btn>
    <v-btn icon>
        <v-icon>more_vert</v-icon>
    </v-btn>
  </v-toolbar>
</template>
<script>
export default {
  name: 'Toolbar'
}


</script>
