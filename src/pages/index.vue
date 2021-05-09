<template>
  <div >
    <v-img :height="200" src="@/assets/sobremi.jpg"></v-img>
    <v-container >
      <v-row >
        <v-col cols=12 class="text-center">
    <h1 class="text-xs-h2 text-md-h1">¿Necesitas un desarrollador?</h1>
    </v-col>
    <v-col cols=12 class="text-center">
    <v-btn color="primary" outlined @click="dialog=true">Quiero saber más
      <v-icon>mdi-emoticon-happy-outline</v-icon>
    </v-btn>
    </v-col>
    <v-col cols=12 class="text-center">
    <v-btn color="primary" @click="sendMail()" outlined>Contacto
      <v-icon>mdi-email-outline</v-icon>
    </v-btn>
    </v-col>
      </v-row>
<v-dialog
        v-model="dialog"
        max-width="600"
        transition="dialog-bottom-transition"
      >
        <dialog-sobre-mi @cerrar="dialog=false"/>
      </v-dialog>
    </v-container>
  </div>
</template>

<script>
// @ is an alias to /src
import dialogSobreMi from "@/components/dialogSobreMi"
export default {
  name: "home",
  components: {
    dialogSobreMi
  },
  data: () => ({
    dialog:false
  }),
  methods:{
    sendMail(){
      window.location.href='mailto:gonzalo.cuadrado.uriel@gmail.com';
    }
  }
};
</script>
