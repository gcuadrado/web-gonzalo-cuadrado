<template>
  <div>
    <v-app-bar color="primary" dark>
      <v-app-bar-nav-icon @click.stop="drawer = !drawer"></v-app-bar-nav-icon>

      <v-toolbar-title>
        <router-link to="/" tag="span" style="cursor: pointer">
          <v-row>
            <v-col>
              <v-avatar>
                <img src="@/assets/avatarGonzalo.png" />
              </v-avatar>
            </v-col>
            <v-col>
              <v-img width="200" src="@/assets/nombre.png" />
            </v-col>
          </v-row> </router-link
      ></v-toolbar-title>

      <v-spacer></v-spacer>
    </v-app-bar>

    <v-navigation-drawer v-model="drawer" absolute temporary>
      <v-list nav dense>
        <v-list-item-group
          v-model="group"
          active-class="blue--text text--accent-4"
        >
          <v-list-item @click="$router.push({ path: '/formacion' })">
            <v-list-item-title>Formación</v-list-item-title>
          </v-list-item>

          <v-list-item @click="$router.push({ path: '/experiencia' })">
            <v-list-item-title>Experiencia</v-list-item-title>
          </v-list-item>

          <v-list-item @click="$router.push({ path: '/proyectos' })">
            <v-list-item-title>Proyectos</v-list-item-title>
          </v-list-item>
        </v-list-item-group>
      </v-list>
    </v-navigation-drawer>
  </div>
</template>
<script>
export default {
  data: () => ({
    drawer: false,
    group: null,
  }),

  watch: {
    group() {
      this.drawer = false;
    },
  },
};
</script>
