<template>
  <div class="box">
    <slot></slot>
  </div>
</template>
<script>
export default {
  name: 'Box'
}
</script>

<style>
 .box {
   border: 3px solid #F69320;
 }
</style>
