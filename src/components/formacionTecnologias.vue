<template>
    <v-card>
    <v-card-title>Tecnologías</v-card-title>
<v-row>
      <v-col sm=4 md=3 class="text-center" v-for="item in items" v-bind:key="item.id">
    
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
          title: "C#",
          subtitle: "",
          avatar: "csharp.jpg",
        },
        {
          id: 4,
          title: "Javascript",
          subtitle: "",
          avatar: "javascript.png",
        },
        {
          id: 5,
          title: "Visual Basic",
          subtitle: "",
          avatar: "vbnet.png",
        },
        {
          id: 6,
          title: "MySQL",
          subtitle: "",
          avatar: "mysql.png",
        },
        {
          id: 7,
          title: "SQL Server",
          subtitle: "",
          avatar: "sqlserver.png",
        },
        {
          id: 8,
          title: "Hibernate",
          subtitle: "",
          avatar: "hibernate.png",
        },
        {
          id: 9,
          title: "Vue",
          subtitle: "",
          avatar: "vue.png",
        },
        {
          id: 10,
          title: "Jarkarta EE",
          subtitle: "",
          avatar: "jakarta.png",
        }
        ,
      ]
        }
    }
}
</script>