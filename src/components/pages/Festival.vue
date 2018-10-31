<template>
  <v-container fluid no-padding bg fill-height grid-list-md id="itfest-jumbotron" class="toolbar-force-opaque toolbar-force-white">
    <v-layout row wrap align-center justify-center>
      <v-flex>
        <div align="center">
          <b style="letter-spacing: 4px;">ARKAVIDIA 5.0 PRESENTS</b>
          <div class="heading-title">
            <h1 class="heading-yellow heading-xlarge margin-bottom-sm futura-bt">IT FESTIVAL</h1>
            <h1 class="shadow heading-xlarge margin-bottom-sm futura-bt">IT FESTIVAL</h1>
          </div>
        </div>
      </v-flex>
    </v-layout>
  </v-container>
  <!--<v-container bg fill-height grid-list-md text-xs-center>
    <v-layout row wrap align-center>
      <v-flex>
        Hello I am center to vertically using "align-center".
      </v-flex>
    </v-layout>
  </v-container>-->
</template>

<script>
export default {
  name: 'Festival',
  props: {
    msg: String
  }
}

</script>
<style type="text/css">
  #itfest-jumbotron {
    height: 100vh;
    margin-top: 0 !important;
    background: #01E8E8;
  }

  .heading-title {
    position: relative;
    min-width: 240px;
  }

  .heading-title > .heading-yellow {
    color: #FFD900;
    -webkit-text-stroke-width: 2px;
    -webkit-text-stroke-color: #444;
    position: absolute;
    margin-top: 5px;
    margin-left: 5px;
    top: auto;
    left: auto;
    width: auto;
    display: inline-block;
  }

  .heading-title > .shadow {
    color: #1DE9EB;
    -webkit-text-stroke-width: 2px;
    -webkit-text-stroke-color: #444;
    display: inline-block;
    z-index: 2;
  }
</style>