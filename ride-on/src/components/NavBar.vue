<template>
            <div>
    <v-toolbar
      white
      prominent
      class="bg-white"
    >
    <v-spacer></v-spacer>
      <v-toolbar-l class="" style="padding:20px;">
          <v-img
  :width="100" 
  aspect-ratio="16/9"
  cover
  src="../assets/logo.jpg"
 style="margin:0 10px;"></v-img>
     </v-toolbar-l>

     
     
     
      <v-spacer></v-spacer>
      <v-btn class="drive hoverme mr-2" color="white">become a driver</v-btn>
      <v-btn class="hoverme mr-2">ride</v-btn>
      <v-btn class="hoverme mr-2">help</v-btn>
      <v-btn class="hoverme mr-2">sign up</v-btn>
<span class="font-weight-bold ">SIGN IN</span>
      <v-btn icon class="hoverme">
        <v-icon>mdi-account-circle</v-icon>
      </v-btn>
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
      
<v-nav class=""><ul class="d-flex ">
         <v-btn  class="hovermes"> <v-icon icon="mdi-home" />Home</v-btn>
         <v-btn class="hovermes "><v-icon class="hovermes ">mdi-information</v-icon> About</v-btn>
         <v-btn class="hovermes  "><v-icon class="hovermes">mdi-car-cog</v-icon>Services</v-btn>
         <v-btn class="hovermes  "><v-icon class="hovermes">mdi-car-connected</v-icon>Our Rides</v-btn>
         <v-btn class="hovermes  "><v-icon class="hovermes">mdi-phone</v-icon>Contact</v-btn>
                  
</ul></v-nav>
    

<v-spacer></v-spacer>

   
    </v-toolbar>
  </div>
       
</template>

<script>
export default {
name: 'NavBar',


data() {
          return {
      hover: false,
    };
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
}
.hovermes:hover{
          color: orange;
}

 img{
          width: 100%;
}
 img:hover{
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