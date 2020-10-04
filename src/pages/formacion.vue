<template>
<div>
 <v-img src="@/assets/educacion.jpg" class="text-center align-center" height="200">
 <p class="text-h2 text-md-h1"><span class="px-2 white">FORMACIÓN</span></p>
 </v-img>
  <v-container>
     
    <v-row>
      <v-col md=6 sm=12>
        <formacion-academica />
      </v-col>
      <v-col md=6 sm=12>
          <formacion-complementaria/>
      </v-col>
    </v-row>
    <v-row>
        <v-col md=12 sm=12>
          <formacion-tecnologias/>
      </v-col> 
    </v-row>
  </v-container>
</div>
</template>
<script>
import formacionAcademica from "@/components/formacionAcademica";
import formacionComplementaria from "@/components/formacionComplementaria";
import formacionTecnologias from "@/components/formacionTecnologias";
export default {
  components: {
    formacionAcademica,
    formacionComplementaria,
    formacionTecnologias
  },
  data() {
    return {};
  },
  methods: {},
};
</script>
