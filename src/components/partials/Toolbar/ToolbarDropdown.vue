<template>
  <v-menu offset-y>
    <v-btn flat slot="activator">
      {{title}}
      <v-icon>arrow_drop_down</v-icon>
    </v-btn>
    <v-list>
      <v-list-tile
        v-for="(item, index) in items" :key="index" :to=item.to>
        <v-list-tile-title>{{ item.title }}</v-list-tile-title>
      </v-list-tile>
    </v-list>
  </v-menu>
</template>
<script>
export default {
  name: 'ToolbarDropdown',
  props: ["items","title"]
}
</script>

<style scoped>
  .v-list__tile--active>.v-list__tile__title {
    color: red !important;
  }
  .v-list.theme--light {
    background: #FFFEF2;
  }
  .v-list.theme--dark{
    background: #04464F;
  }
</style>
