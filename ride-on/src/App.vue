<template>
  <v-app>
    <NavBar />
    <v-main>
      <router-view/>
    </v-main>
    <FooterView />
    <FooterApp />
  </v-app>
</template>

<script>
import NavBar from './components/NavBar.vue'
import FooterApp from './components/FooterApp.vue'

export default {
  name: 'App',
components: {
 NavBar,
 FooterApp,

},


  data: () => ({
    //
  }),
}
</script>
