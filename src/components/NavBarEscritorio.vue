<template>
    <v-app-bar
      app
      color="primary"
      dark
    >
    <v-avatar>
      <img
        src="@/assets/avatarGonzalo.png"
        @click="$router.push({path:'/'})"
      >
    </v-avatar>


        <v-toolbar-title>Gonzalo Cuadrado Uriel</v-toolbar-title>


      <v-spacer></v-spacer>

      <v-btn
        @click="$router.push({path:'/formacion'})"
        target="_blank"
        text
      >
        <span class="mr-2">Formación</span>
        <v-icon>mdi-book-open-variant</v-icon>
      </v-btn>
      <v-btn
        href="https://github.com/vuetifyjs/vuetify/releases/latest"
        target="_blank"
        text
      >
        <span class="mr-2">Experiencia</span>
        <v-icon>mdi-briefcase</v-icon>
      </v-btn>
      <v-btn
        href="https://github.com/vuetifyjs/vuetify/releases/latest"
        target="_blank"
        text
      >
        <span class="mr-2">Proyectos</span>
        <v-icon>mdi-laptop-chromebook</v-icon>
      </v-btn>
    </v-app-bar>
</template>
<script>
export default {
    
}
</script>