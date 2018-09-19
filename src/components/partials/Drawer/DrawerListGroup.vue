<template>
  <v-list-group
    no-action
  >
    <v-list-tile slot="activator">
      <v-list-tile-title>{{title}}</v-list-tile-title>
    </v-list-tile>
    <router-link 
      v-for="item in items"
      :key= "item.title"
      :to=item.to
      class="no-decoration"
    >
      <v-list-tile>
        <v-list-tile-content>
          <v-list-tile-title>{{item.title}}</v-list-tile-title>
        </v-list-tile-content>
      </v-list-tile>
    </router-link>
  </v-list-group>
</template>

<script>
export default {
    name: 'DrawerListItem',
    props: [ "items", "title"]
}
</script>
