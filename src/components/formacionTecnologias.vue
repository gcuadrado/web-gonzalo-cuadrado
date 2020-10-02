<template>
    <v-card>
    <v-card-title>Tecnologías</v-card-title>
<v-row>
      <v-col class="text-center" v-for="item in items" v-bind:key="item.id">
    
          <v-avatar size="60" rounded color="white">
            <img :src="require('@/assets/' + item.avatar)" />
          </v-avatar>
            <p>{{item.title}}</p>
      </v-col>
</v-row>
</v-card>
</template>
<script>
export default {
    data(){
        return{
items: [
        {
          id: 1,
          title: "Java",
          subtitle: "",
          avatar: "java.jpg",
        },
        {
          id: 2,
          title: "Android",
          subtitle: "",
          avatar: "android.png",
        },
        {
          id: 3,
          title: "MySQL",
          subtitle: "",
          avatar: "mysql.png",
        },
        {
          id: 4,
          title: "SQL Server",
          subtitle: "",
          avatar: "sqlserver.png",
        },
      ]
        }
    }
}
</script>