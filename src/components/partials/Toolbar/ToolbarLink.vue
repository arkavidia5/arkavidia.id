<template>
  <v-btn flat :to=to :href=href>{{title}}</v-btn>
</template>
<script>
export default {
  name: 'ToolbarLink',
  props: ["to","title","href"]
}
</script>

<style scoped>
  .v-btn:focus:before, .v-btn:hover:before {
      background: transparent;
  }
  .v-btn--active {
    color: red;
  }
  .v-btn--active:before {
    background: transparent;
  }
</style>
