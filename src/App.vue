<template>
  <v-app>
    <nav-bar-escritorio v-if="!$vuetify.breakpoint.mobile"/>
    <nav-bar-movil v-else/>
    <v-main>
      <router-view/>
    </v-main>
    <Footer/>
  </v-app>
</template>

<script>
import NavBarEscritorio from './components/NavBarEscritorio'
import NavBarMovil from './components/NavBarMovil'
import Footer from './components/Footer'
//import 'bootstrap/dist/css/bootstrap.css'
//import 'bootstrap-vue/dist/bootstrap-vue.css'

export default {
  name: 'App',

  components: {
    NavBarEscritorio,
    NavBarMovil,
    Footer
  },

  data: () => ({
    //
  }),
};
</script>
