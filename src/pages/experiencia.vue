<template>
  <div>
    <v-img
      class="text-center align-center"
      src="https://blog.worktel.com/wp-content/uploads/2017/04/business-people-working-office-corporate-team-concept-56298931.jpg"
      height="200"
    >
      <p class="text-h2 text-md-h1">
        <span class="px-2 bg-light">EXPERIENCIA</span>
      </p>
    </v-img>
    <v-card class="mx-auto">
      <v-container>
        <v-row dense>
          <v-col v-for="card in cards" :key="card.title" :cols="card.flex">
            <v-card>
              <v-img
                :src="card.src"
                class="white--text align-end"
                height="200px"
              >
                <v-card-title
                  class="display-1 font-weight-light black--text mb-2"
                  ><span class="bg-light">{{ card.title }}</span></v-card-title
                >
              </v-img>

              <v-card-actions>
                <v-card-subtitle
                  class="text-h6"
                  v-text="card.subtitle"
                ></v-card-subtitle>
                <v-spacer></v-spacer>
              </v-card-actions>
            </v-card>
          </v-col>
        </v-row>
      </v-container>
    </v-card>
  </div>
</template>
<script>
export default {
  data: () => ({
    cards: [
      {
        title: "Smartlabs S.L.",
        subtitle: "Programador ASP.NET (C# y VB.NET) y Vue.js",
        src: "https://www.smartlabs.es/img/servicios/reparacion.png",
        flex: 12,
      },
      {
        title: "El Androide Libre",
        subtitle: "Redactor de tecnología",
        src:
          "https://images-na.ssl-images-amazon.com/images/I/919fclOv76L._AC_SL1500_.jpg",
        flex: 12,
      },
      {
        title: "Proyectos propios",
        subtitle: "Aplicaciones Android nativas, backend y aplicaciones web",
        src:
          "https://www.ecestaticos.com/imagestatic/clipping/876/f60/876f604c1dda237be9ed0feb004e1229/conoces-a-un-analista-programador-si-le-recomiendas-y-le-fichan-te-llevas-2-ooo.jpg?mtime=1579565836",
        flex: 12,
      },
    ],
  }),
};
</script>