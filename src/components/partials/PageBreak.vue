<template>
  <div class="page-break__wrapper">
    <div class="page-break">
      <div class="line"></div>
      <div class="circle">
        <div class="inner-circle"></div>
      </div>
      <div class="line"></div>
    </div>
  </div>
</template>
<script>
export default {
  name: 'PageBreak',
}
</script>

<style scoped> 
  .page-break__wrapper {
    display: flex;
    justify-content: center;
  }
  .page-break {
    padding: 30px;
    width: 70%;
    height: 30px;
    display: flex;
    align-items: center;
  }
  .line {
    width: 45%;
    height: 5px;
    background: #04464F;
  }
  .circle {
    width: 10%;
    display: flex;
    justify-content: center;
    align-items: center;
  }
  .inner-circle {
    width: 30px;
    height: 30px;
    border: 3px solid #179FA4;
    border-radius: 50%;
  }
</style>

