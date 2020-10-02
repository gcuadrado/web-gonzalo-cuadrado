<template>
  <v-app>
    <nav-bar-escritorio v-if="!$vuetify.breakpoint.mobile"/>
    <nav-bar-movil v-else/>
    <v-main>
      <router-view/>
    </v-main>
  </v-app>
</template>

<script>
import NavBarEscritorio from './components/NavBarEscritorio'
import NavBarMovil from './components/NavBarMovil'

export default {
  name: 'App',

  components: {
    NavBarEscritorio,
    NavBarMovil
  },

  data: () => ({
    //
  }),
};
</script>
