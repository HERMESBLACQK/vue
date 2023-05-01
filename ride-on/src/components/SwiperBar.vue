<template>
<Swiper class="testimonial pa-16 "
:modules="modules"
space-between="50"
loop="true"
:pagination="{clickable: true}"
navigation
grab-cursor
slides-per-view="1"

>
<Swiper-slide  class="pa-4 text-center bg-white w-50" v-for="lot in swiperText" :key="lot">
  <v-card-title class="d-flex justify-center ">

<v-card-img class="card-pic pa-4 w-15 d-flex justify-center mx-16 bg-pink-lighten-5" variant-outlined>
  <v-img
  :width="70" 
  aspect-ratio="4/3"
  cover
  height="100%"
  src="../assets/2cars.png" class=" "
></v-img>
  </v-card-img>
</v-card-title>
<v-card-subtitle class="text-md-h6 font-weight-bold text-black">

  <h4>{{ lot.Name }}</h4>
</v-card-subtitle>
  <v-card-text>
    {{ lot.Text }}
  </v-card-text>
  <v-card-foot >
    <v-icon class="text-orange">

      {{ lot.icon }}
    </v-icon>
    <v-icon class="text-orange">

      {{ lot.icon }}
    </v-icon>
    <v-icon class="text-orange">

      {{ lot.icon }}
    </v-icon>
    <v-icon class="text-orange">

      {{ lot.icon }}
    </v-icon>
    <v-icon class="text-orange">

      {{ lot.icon }}
    </v-icon>
   
  </v-card-foot>
</Swiper-slide>





</swiper>
</template>

<script>

import { Swiper, SwiperSlide} from 'swiper/vue'
import {  Pagination, Navigation,} from 'swiper'
import 'swiper/css'
import 'swiper/css/pagination'
import 'swiper/css/navigation'
import {ref} from 'vue'

export default {

  name: 'SwiperBar',
  components: {Swiper, SwiperSlide},
setup() {






  const swiperText = ref (  [
    {
      Text: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Molestiae doloribus tenetur provident blanditiis excepturi tempora in exercitationem repellendus, libero reprehenderit.', Name: ' Milner', icon: 'mdi-star',  img: './assets/2cars.png'
    },
    {
      Text: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Molestiae doloribus tenetur provident blanditiis excepturi tempora in exercitationem repellendus, libero reprehenderit.', Name: 'john Milner', icon: 'mdi-star'
    },
    {
      Text: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Molestiae doloribus tenetur provident blanditiis excepturi tempora in exercitationem repellendus, libero reprehenderit.', Name: ' Milner', icon: 'mdi-star'
    },
    {
      Text: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Molestiae doloribus tenetur provident blanditiis excepturi tempora in exercitationem repellendus, libero reprehenderit.', Name: 'jude Milner', icon: 'mdi-star'
    }
  ] 
  );

  return {
    modules: [ Pagination, Navigation, ], swiperText
  }
}


};

</script>

<style>

</style>