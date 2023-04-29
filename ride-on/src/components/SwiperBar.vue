
<template>
          <div>
           swipe
      
          </div>
          <v-container fluid class="testimonial pa-12 text-center d-flex justify-center">
    <v-card bg-white flat class="pa-8 w-50 text-center" v-for="lot in box" :key="lot">
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
   
     <h4>James Milner</h4>
   </v-card-subtitle>
     <v-card-text>
       {{ lot.text }}
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
    </v-card>
   
   
   </v-container>
   <swiper
       :modules="modules"
       :slides-per-view="3"
       :space-between="50"
       navigation
       :pagination="{ clickable: true }"
       :scrollbar="{ draggable: true }"
       @swiper="onSwiper"
       @slideChange="onSlideChange"
     >
       <swiper-slide>Slide 1</swiper-slide>
       <swiper-slide>Slide 2</swiper-slide>
       <swiper-slide>Slide 3</swiper-slide>
       ...
     </swiper>
           </template>
           
           <script>
           import { Navigation, Pagination, Scrollbar, A11y } from 'swiper';
   
   // Import Swiper Vue.js components
   import { Swiper, SwiperSlide } from 'swiper/vue';
   
   // Import Swiper styles
   import 'swiper/css';
   import 'swiper/css/navigation';
   import 'swiper/css/pagination';
   import 'swiper/css/scrollbar';
           
             export default {
              name: 'SwiperBar',
              components: {
         Swiper,
         SwiperSlide,
       },
   
             
              data () {
   return {
   
     box: [
     {id: 1,  text: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Molestiae doloribus tenetur provident blanditiis excepturi tempora in exercitationem repellendus, libero reprehenderit.', icon: 'mdi-star'}
   ]
     
   }
     },
   
       setup() {
         const onSwiper = (swiper) => {
           console.log(swiper);
         };
         const onSlideChange = () => {
           console.log('slide change');
         };
         return {
           onSwiper,
           onSlideChange,
           modules: [Navigation, Pagination, Scrollbar, A11y],
         };
       },
              }
             
             
           </script>