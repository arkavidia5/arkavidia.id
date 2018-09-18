<template>
  <v-container fluid no-padding>
    <v-slide-y-transition mode="out-in">
      <v-responsive :aspect-ratio="1.60 " class="row about-background">
        <!-- <v-layout row justify-center>
          <iframe style="width:70%" src="https://www.youtube.com/embed/ppVvsgQhBGM" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen></iframe>
        </v-layout> -->
        <v-container>
          <v-layout row>
            <v-flex xs10 offset-xs1 >
              <h1 class="heading" align="center">About Arkavidia</h1>
              <p class="text-xs-center">
                Arkavidia Informatics & IT Festival merupakan serangkaian acara IT skala nasional yang diharapkan dapat menginspirasi dan memberikan wawasan baru untuk masyarakat, serta dapat memberikan dampak positif untuk Indonesia.
              </p>
              <br>
              <h1 class="heading" align="center">
                Visi
              </h1>
              <p class="text-xs-center">
                Arkavidia sebagai pergerakan untuk menginspirasi pelajar, mahasiswa, dan masyarakat Indonesia dalam menjawab tantangan global di bidang IT.
              </p>
              <br>
              <h1 class="heading" align="center ">
                Misi
              </h1>
              <p>
                <ul class="yellow-dash">
                  <li>Memperkenalkan teknologi terkini di berbagai bidang di kalangan pelajar dan mahasiswa.</li>
                  <li>Meningkatkan partisipasi pelajar dan mahasiswa di kompetisi nasional.</li>
                  <li>Meningkatkan wawasan pelajar, mahasiswa, dan masyarakat Indonesia di bidang IT</li>
                </ul>
              </p>
            </v-flex>
          </v-layout>
        </v-container>
      </v-responsive>
    </v-slide-y-transition>
  </v-container>
</template>

<script>
export default {
  name: 'About',
  props: {
    msg: String
  },
  methods: {
    getHeight() {
      return 100; 
    }
  }
}
</script>

<style scoped>
  * {
  font-size: 1.5rem; 
  }
  .about-background {
    margin-top: 30px;
    background: url('../../assets/export-background.svg');
    background-size: 101%;
    background-position: center top;
    background-repeat: no-repeat;  
    
  }
  .yellow-dash {
    list-style-type: dash;
    list-style-image: url('../../assets/minus-symbol.svg')
  }
</style>
