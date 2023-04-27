<template>
  <v-app>
    <NavBar />
    <v-main>
      <router-view/>
    </v-main>
    <FooterView />
  </v-app>
</template>

<script>
import NavBar from './components/NavBar.vue'
import FooterView from './components/FooterView.vue'

export default {
  name: 'App',
components: {
 NavBar,
 FooterView
},


  data: () => ({
    //
  }),
}
</script>
