<template>
<v-card>
    <v-card-title>Formación Académica</v-card-title>
   <v-timeline align-top dense>
      <v-timeline-item small v-for="item in items" v-bind:key="item.id">
        <template v-slot:icon>
          <v-avatar size="60" color="white">
            <img :src="require('@/assets/' + item.avatar)" />
          </v-avatar>
        </template>
        <v-row class="pt-1">
          <v-col cols="3">
            <strong>{{ item.year }}</strong>
          </v-col>
          <v-col>
            <strong>{{ item.title }}</strong>
            <div class="caption">
              {{ item.subtitle }}
            </div>
          </v-col>
        </v-row>
      </v-timeline-item>
    </v-timeline> 
</v-card>
</template>
<script>
export default {
    data(){
        return{
items: [
        {
          id: 1,
          year: "2012",
          title: "Bachillerato en Ciencias Sociales",
          subtitle: "IES Profesor Julio Pérez",
          avatar: "julioperez.png",
        },
        {
          id: 2,
          year: "2017",
          title: "Grado en Historia",
          subtitle: "Universidad Rey Juan Carlos",
          avatar: "urjc.png",
        },
        {
          id: 3,
          year: "2018",
          title: "Máster en Formación del profesorado",
          subtitle: "Universidad Rey Juan Carlos",
          avatar: "urjc.png",
        },
        {
          id: 4,
          year: "2020",
          title: "CFGS en Desarrollo de Aplicaciones Multiplataforma",
          subtitle: "IES Francisco de Quevedo",
          avatar: "quevedo.jpg",
        },
      ]
        }
    }
}
</script>