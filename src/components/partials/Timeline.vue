<template>
    <div class="timeline-container">
      <slot/>
    </div>
</template>
<script>
export default {
    name: 'Timeline'
}
</script>
<style scoped>
    .timeline-container {
        width: 100%;
    }
</style>
