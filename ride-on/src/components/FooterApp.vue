<template>
     <v-footer class="bg-black">
    <v-row justify="space-around" class="d-flex pl-8" no-gutters>
      <v-col class="text-center mt-4 " cols="" v-for="first in first" :key="first">
<v-card-title><h2>{{ first.title }}<v-span class="text-orange">{{ first.sub }}</v-span> </h2></v-card-title>
<v-card-text class="text-4 font-weight-light text-body-2">
 <p>{{ first.text }} </p>
</v-card-text>
<v-card-subtitle class="ma-0 text-md-h6">
  <h5 class="mt-0">{{ first.free }} <v-span class="text-orange mt-0">{{ first.freesub }}</v-span></h5> 
</v-card-subtitle>
<v-card-text class=" mt-2"> <v-icon class="text-orange">{{ first.icon }}</v-icon> {{ first.phone }}</v-card-text>
        
      </v-col>
    
      <v-col class="text-center mt-4 ml-2" cols="">
    <v-card-title>
      <h3>Useful Links</h3>
    </v-card-title>
    <v-card-content class="d-flex justify-center">
      <v-card-items class="d-block justify-center">
      <v-ul-title></v-ul-title>
      <v-ul class="pr-2 d-block " v-for="list in second" :key="list">
        <v-list class="d-block pa-2 text-body-2 bg-black hoverme">
          {{ list.list }}
        </v-list >
   
      </v-ul>
  
    </v-card-items>
    <v-card-items>

   
      <v-ul class="pr-2 d-block " v-for="third in third" :key="third">
        <v-list class="d-block col pa-2 text-body-2 bg-black hoverme">
          {{ third.list }}
        </v-list >
   
    
      </v-ul>
    </v-card-items>
    </v-card-content>
   
      </v-col>
      <v-col class="text-center mt-4" cols="" v-for="list in fourth" :key="list">
        <v-card-title>
      <h3>{{ list.title }}</h3>
    </v-card-title>
<v-card-text class="text-body-2 font-weight-light ma-0 pa-1">
 {{ list.text }}
</v-card-text>
<v-card-text class="text-body-2 font-weight-light ma-0 pa-1">
{{ list.email }}
</v-card-text>
<v-card-text class="text-body-2 font-weight-light ma-0 pa-1">
{{ list.fax }}
</v-card-text>
<v-card-text class="text-body-2 font-weight-light ma-0 pa-1">
{{ list.phone }}
</v-card-text>


      </v-col>
      <v-col class=" text-center mt-4 " variant="" cols="">
        <v-card-title class="">
      <h3>Download Mobile App</h3>
    </v-card-title>
    <v-card-item class=" justify-center ">
<v-card-img class="d-block mx-2">
  <v-img
  :width="150" 
  aspect-ratio="16/9"
  cover
  height="100%"
  src="../assets/apple.png" class=" mx-2 "
></v-img>
<v-img
  :width="150" 
  aspect-ratio="16/9"
  cover
  height="100%"
  src="../assets/google2.png" class="mx-2 "
></v-img>
</v-card-img>
<v-card-text class="px-4">
  <!-- <v-btn variant="outlined" class="bg-black  w-100 my-2 px-6 text-center align-center">Become a Driver</v-btn>
<v-btn variant="outlined" class="bg-black  w-100 my-2 px-6 text-center align-center">Become a Driver</v-btn> -->
</v-card-text>


    </v-card-item>
   
      </v-col>
    </v-row>
  </v-footer>
</template>

<script>
export default {
name: 'FooterApp',

data () {
  return{
    first:[
      {title: 'TAXI', sub: 'GEO', text: 'Lorem ipsum dolor sit amet, consectetur adipisicing elit. Architecto hic minus veniam dicta itaque magni neque quam recusandae, atque dolorum ipsa culpa similique delectus explicabo ipsam voluptate voluptatum,', free: 'Toll Free', freesub: 'Helpline', icon: 'mdi-phone', phone: '(+234)9035355746'}
    ],
    second: [
      {list: 'Home'},
      {list: 'About'},
      {list: 'Services'},
      {list: ' Our Rides'},
      {list: 'Contact'}
    ],
    third: [
      {list: 'Ride'},
      {list: 'Become a Driver'},
      {list: 'Help'},
      {list: 'Privacy Policy'},
      {list: 'Terms And Conditions'}
    ],
    fourth:[
      {title: 'Head Office', text: ' 3 Apatapiti Street, Futa Southgate, Akure, Ondo State, Nigeria.', email: 'Email Address: Dr.blacqk@gmail.com', fax: 'Fax: Service@hermestech.com',  phone: 'Phone Number: (+234)9035355746'}
    ]
  }
}

}
</script>

<style>
 .fb-btn{
  border: 2px solid white;
  color: #f3dde1;
 }

</style>