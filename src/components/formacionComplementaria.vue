<template>
<v-card>
    <v-card-title>Formación Complementaria</v-card-title>
   <v-timeline align-top dense>
      <v-timeline-item small v-for="item in items" v-bind:key="item.id">
        <template v-slot:icon>
          <v-avatar size="60" rounded color="white">
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
          year: "2013",
          title: "Microsoft Word Office Specialist",
          subtitle: "Microsoft",
          avatar: "word.png",
        },
        {
          id: 2,
          year: "2018",
          title: "Java + Android (400h)",
          subtitle: "Ayuntamiento de Rivas-Vaciamadrid",
          avatar: "java-android.png",
        },
        {
          id: 3,
          year: "2016",
          title: "TOEIC Inglés B1",
          subtitle: "Capman",
          avatar: "toeic.png",
        }
      ]
        }
    }
}
</script>