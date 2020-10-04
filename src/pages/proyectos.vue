<template>
  <div>
       <v-img src="https://lh3.googleusercontent.com/proxy/Wtq_AMSV0nY77uhJvX8twShzkk5S6ySkbWJIkLKQID0vEnb4piQwFStwIRvOzzHMqKR1s8q1XjOKaOioFnjBS919lCpvo46zNLoT4d5pmXtia1kY-5eoWPEO0DlD41mDDrm5kg" class="text-center align-center" height="200">
 <p class="text-h2 text-md-h1"><span class="px-2 white">PROYECTOS</span></p>
       </v-img>
    <v-container>
        <v-row>
            <v-col  v-for="proyecto in proyectos"
        v-bind:key="proyecto.id">
      <v-card
        class="mx-auto px-5"
        outlined
       
      >
        <v-row>
          <v-col cols="9">
            <v-card-title class="headline mb-1">
              {{ proyecto.nombre }}
            </v-card-title>
            <v-card-subtitle>{{ proyecto.descripcion }}</v-card-subtitle>
          </v-col>
          <v-col cols="3" class="justify-center">
            <v-avatar  size="70">
              <v-img :src="require('@/assets/proyectos/'+proyecto.logo)"></v-img>
            </v-avatar>
          </v-col>
        </v-row>
        <v-row >
          <v-col
          v-for="imagen in proyecto.imagenes"
          v-bind:key="imagen"
          :cols="12/proyecto.imagenes.length"
          >
            <v-img
              :src="require('@/assets/proyectos/'+imagen)"
            ></v-img>
          </v-col>
        </v-row>

        <v-card-actions>
          <v-btn target="_blank" :href="proyecto.descarga" outlined rounded text> DESCARGA EN GOOGLE PLAY </v-btn>
          <v-btn v-if="proyecto.github!==null" target="_blank" :href="proyecto.github" outlined rounded text> CÓDIGO FUENTE </v-btn>
        </v-card-actions>
        <v-chip
          class="ma-2"
          color="pink"
          label
          small
          text-color="white"
          v-for="tec in proyecto.tecnologias"
          v-bind:key="tec"
        >
          <v-icon left> mdi-label </v-icon>
          {{ tec }}
        </v-chip>
      </v-card>
            </v-col>
        </v-row>
    </v-container>
  </div>
</template>
<script>
export default {
  data() {
    return {
      proyectos: [
        {
          id: 1,
          nombre: "#DescubreRivas",
          tecnologias: ["Android", "Java", "MySQL","PHP"],
          descripcion:
            "Aplicación nativa Android, escrita en Java, que señala los puntos de interés histórico de la ciudad",
          descarga: "https://play.google.com/store/apps/details?id=com.turismorivas&hl=es",
          github: null,
          logo: "descubrerivas/logo.webp",
          imagenes:["descubrerivas/1.webp","descubrerivas/2.webp","descubrerivas/3.webp"]
        },
        {
          id: 2,
          nombre: "#DescubreEspaña",
          tecnologias:["Android","Java","JakartaEE","MySQL","JAX-RS"],
          descripcion: "Aplicación nativa Android y servicio web Java",
          descarga: "https://play.google.com/store/apps/details?id=es.iesquevedo.descubreespana&hl=es",
          github: null,
          logo: "descubreespana/logo.webp",
          imagenes:["descubreespana/1.webp","descubreespana/2.webp","descubreespana/3.webp"]

        },
        {
          id: 3,
          nombre: "Digi Connect",
          descripcion: "Aplicación nativa Android que hace uso de WebView, Widgets de escritorio, desbloqueo por huella etc...",
          descarga: "https://play.google.com/store/apps/details?id=com.connect.digi&hl=es",
          github: null,
          logo: "digiconnect/logo.webp",
          imagenes:["digiconnect/1.webp","digiconnect/2.webp","digiconnect/3.webp"]
        },
      ],
    };
  },
};
</script>