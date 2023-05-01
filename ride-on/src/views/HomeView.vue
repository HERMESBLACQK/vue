<template>
<v-container fluid class="check pa-2 bg-orange-lighten-5" >
  <v-row class="">
    <v-col class="bg-orange pa-8 scale">
<v-col-item class="float-right text-h2 py-16 ml-16" v-for="text in header" :key="text">
  <h4 class="float-right ma-2">{{ text.title }}</h4>
  <p class="text-body-2 my-2 mt-4">{{ text.text }}</p>
  <v-btn class="fades float-center bg-black">{{ text.cont}}</v-btn>
</v-col-item>     
    
    </v-col>
    <v-col class=" pa-8 pt-16">
      <v-card-img class="d-flex mx-2">

<v-img
  :width="150" 
  aspect-ratio="4/3"
  cover
  height="100%"
  src="../assets/benz.png" class="mt-16 "
></v-img>
</v-card-img>
    </v-col>
  </v-row>
</v-container>
<v-container justify-center class="text-center py-16">
  <v-title><h2 class="">How it works</h2>
  <h3 class="work"></h3></v-title>
  <v-row d-flex  class="px-4 mt-16" >
    <v-col class="pa-4" v-for="item in order" :key="item">
<v-card  class="pa-2">
  <v-card-img class="card-pic pa-4 w-25 d-flex justify-center mx-16 bg-pink-lighten-5" variant-outlined>
 <v-icon class="">{{ item.icon }}</v-icon>
  </v-card-img>
  <v-card-title>
    {{ item.title }}
  </v-card-title>
  <v-text class="text-body-2 text-center">
  {{ item.text }}
  </v-text>
</v-card>
    </v-col>
  </v-row>
</v-container>
<v-container fluid class=" pa-2 bg-orange-lighten-5" >
  <v-row class="">
    <v-col class=" pa-16 ">
<v-col-item class=" text-h4 py-16" v-for="text in header2" :key="text">
  <h4 class="mb-0">{{ text.title }} </h4>
  <h3 class="mb-8" style="border-bottom: 5px dashed orange; width: 25%;"></h3>
  <p class="text-body-2 my-2 mt-4">{{ text.text }}</p>
  <v-btn flat class="fades bg-black">{{ text.cont}}</v-btn>
</v-col-item>     
    
    </v-col>
    <v-col class=" pa-8 pt-16">
      <v-card-img class="d-flex mx-2">

<v-img
  :width="150" 
  aspect-ratio="4/3"
  cover
  height="100%"
  src="../assets/2cars.png" class="mt-16 "
></v-img>
</v-card-img>
    </v-col>
  </v-row>
</v-container>

<v-container fluid class="testimonial pa-8 text-center d-flex justify-space-between">
 <v-card bg-white  class="pa-8 text-center ma-2" v-for="lot in box" :key="lot">
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

  <h4>{{ lot.name }}</h4>
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



</template>

<script>


export default ({
  name: 'HomeView',

data () {
return {
  header:[
{ title: 'Earn. Connect. Contribute to society', text: 'Partner with us to drive your own livelyhood and more', cont: 'sign up'},

  ],
  header2:[
{ title: 'About Us', text: 'Lorem ipsum, dolor sit amet consectetur adipisicing elit. Corrupti reiciendis voluptatem perspiciatis id! Ipsa odio beatae aut eaque facilis illo dicta alias? Quam et nulla accusamus qui dolorem quasi voluptas, ratione libero. Eius totam quo cupiditate inventore, id excepturi, dicta amet corporis cum dolorum blanditiis odit perferendis veniam sint. Nostrum porro, assumenda, atque magni beatae animi quos quam architecto quasi, eveniet delectus pariatur. Voluptates minima deleniti obcaecati tenetur laboriosam cum fugit quibusdam nemo ratione aperiam, quo amet quia. Numquam accusamus laudantium dolor tempore voluptatem fuga error sint delectus quos consequatur provident perferendis aliquid hic sed laboriosam ab, nesciunt suscipit maiores?', cont: 'Read More'},

  ],
  order: [
    { title: ' Book in a Ride', icon: 'mdi-car', text: '   Lorem ipsum dolor sit amet consectetur adipisicing elit. Itaque recusandae a ipsam repudiandae officia adipisci quidem labore, vitae consequatur'},
    { title: ' Get a Driver', icon: 'mdi-phone-classic', text: '   Lorem ipsum dolor sit amet consectetur adipisicing elit. Itaque recusandae a ipsam repudiandae officia adipisci quidem labore, vitae consequatur'},
    { title: ' Track your Driver', icon: 'mdi-radar', text: '   Lorem ipsum dolor sit amet consectetur adipisicing elit. Itaque recusandae a ipsam repudiandae officia adipisci quidem labore, vitae consequatur'},
    { title: ' Arrive Safely', icon: 'mdi-map-marker-radius', text: '   Lorem ipsum dolor sit amet consectetur adipisicing elit. Itaque recusandae a ipsam repudiandae officia adipisci quidem labore, vitae consequatur'}
  ],
  box: [
  {name: 'john mary',  text: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Molestiae doloribus tenetur provident blanditiis excepturi tempora in exercitationem repellendus, libero reprehenderit.', icon: 'mdi-star'

  
},
  {name: 'john sarah',  text: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Molestiae doloribus tenetur provident blanditiis excepturi tempora in exercitationem repellendus, libero reprehenderit.', icon: 'mdi-star'

  
},
  {name: 'john pauline', text: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Molestiae doloribus tenetur provident blanditiis excepturi tempora in exercitationem repellendus, libero reprehenderit.', icon: 'mdi-star'

  
},
  {name: 'john wendy',  text: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Molestiae doloribus tenetur provident blanditiis excepturi tempora in exercitationem repellendus, libero reprehenderit.', icon: 'mdi-star'

  
}
  ]
}

}

});
</script>


<style>
*{
  padding: 0;
  margin: 0;
  box-sizing: border-box;
}

 .fades:hover{
  background: white;
  color: black;
 }
 .scale{
  margin: 20px 0;
  /* transform: skew(-6deg, 3deg); */
/* border-top-left-radius: 250px; */
border-top-right-radius: 350px;
border-bottom-left-radius: 190px;
border-bottom-right-radius: 190px;
 }
 .card-pic{
  border-radius: 50%;
  /* border: 2px solid red; */
 }
 .work{
  border-bottom: 5px dashed orange;
  width: 10%;
  position: absolute;
  left: 45%;
 }
 .testimonial{
  background-image:linear-gradient(to bottom, rgba(245, 246, 252, 0.52), rgba(117, 19, 93, 0.73)),
    url('../assets/background.jpg');;
  background-size: cover;
  background-repeat: no-repeat;
 }
 .swipeimg{
  border: 1px solid silver;
  border-radius: 50%;
  /* width: 20%; */
  
  
 }
</style>