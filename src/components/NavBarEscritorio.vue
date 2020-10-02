<template>
  <v-app-bar app color="primary" dark>
    <v-toolbar-title>
      <router-link to="/" tag="span" style="cursor: pointer">
        <v-row>
          <v-col>
            <v-avatar>
              <img src="@/assets/avatarGonzalo.png" />
            </v-avatar>
          </v-col>
          <v-col>
            <v-img width="240" src="@/assets/nombre.png" />
          </v-col>
        </v-row> </router-link
    ></v-toolbar-title>

    <v-spacer></v-spacer>

    <v-btn @click="$router.push({ path: '/formacion' })" target="_blank" text>
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
export default {};
</script>