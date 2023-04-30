<template>
            <div app>
    <v-toolbar
      white
      prominent
      class="bg-white"
    app>
    <v-spacer></v-spacer>
      <v-toolbar-l class="img" style="padding:20px;">
          <v-img
  :width="100" 
  aspect-ratio="16/9"
  cover
  src="../assets/logo.jpg"
 style="margin:0 10px;"></v-img>
     </v-toolbar-l>

     
     
     
      <v-spacer></v-spacer>
      <v-list-title v-for="list in headlist" :key="list">

        <v-btn class="drive hoverme mr-2" color="white">{{ list.text }}</v-btn>
      </v-list-title>
      <v-list-title v-for="btn in headbtns" :key="btn">

        <v-btn class="hoverme mr-2">{{btn.text}}</v-btn>
      </v-list-title>
      <v-list-content v-for="cont in headlistcont" :key="cont">

        <span class="font-weight-bold text-uppercase">{{ cont.text }}</span>
              <v-btn icon class="hoverme text-body-2">
                <v-icon>{{ cont.icon }}</v-icon>
              </v-btn>
      </v-list-content>
    </v-toolbar>
  </div>
   <div>
  
    <v-toolbar
      dark
      prominent
     class="bg-black"
    >
 
     <v-spacer></v-spacer>
   <v-toolbar-search class=""> <label class="bg-white" style="padding: 6px 0;">  <v-icon>mdi-map-marker</v-icon></label>
          <input  type="text" placeholder="  Tell us your area" class="bg-white"><label><v-btn style="background-color: orange; border-radius: 0;"><v-icon >mdi-arrow-right</v-icon></v-btn></label>
   </v-toolbar-search>
     <v-spacer></v-spacer>
      
<v-nav class=" d-flex" ><ul class="d-flex " v-for="navlist in navlist" :key="navlist">
         <v-btn  class="hovermes d-flex" > <v-icon>{{ navlist.icon }}</v-icon>{{ navlist.text }}</v-btn>
 
                  
</ul></v-nav>
    

<v-spacer></v-spacer>

   
    </v-toolbar>
  </div>
       
</template>

<script>
export default {
name: 'NavBar',


data() {
   return{
    headbtns: [
      { text: 'Ride', route: '/'},
      { text: 'Help', route: '/'}
    ],
    headlist: [
      { text: 'sign up', route: '/'},
      { text: 'become a driver', route: '/'}
    ],
    navlist: [
      { icon: 'mdi-home', text: 'home', route: '/'},
      { icon: 'mdi-information', text: 'about', route: '/'},
      { icon: 'mdi-car-cog', text: 'Services', route: '/'},
      { icon: 'mdi-car-connected', text: 'Our Rides', route: '/'},
      { icon: 'mdi-phone', text: 'Contact', route: '/'}
    ],
    headlistcont: [
      { icon: 'mdi-account-circle', text: 'sign in', route: '/'}
      // { text: 'become a driver', route: '/'}
    ],
   }
},
methods: {
          hoverMe() {
                   
          }
}
}


</script>

<style>
.drive{
          background: black;
          color: white;
}
.hoverme:hover{
          color: white;
          background: orange;
          cursor: pointer;
}
.hovermes:hover{
          color: orange;
}

 .img img{
          width: 100%;
}
 .img img:hover{
          /* width: 120%; */
          transition-duration: 0.8s;
          cursor: pointer;
          transform: translateX(-30px);
          
}
ul{
          display: flex;
          justify-content: space-between;
}
ul li{
          list-style: none;
          padding: 15px 5px;
          cursor: pointer;
          border: none;
          margin:0 10px;
}
li:hover{
          padding: 15px;
          transition-duration: 0.9s;
          border-radius: 5px;
          background: orange;
          color: white;
}
li a{
          text-decoration: none;
          
}
label{
          display: inline-block;
          align-items: center;
}
input{
          padding:6px;
          border: 1px solid #4f545c;
          background: rgb(202, 201, 201);
          outline:none;
}




</style>