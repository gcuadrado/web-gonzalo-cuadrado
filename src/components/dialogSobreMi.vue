<template>
    <v-container>
        <v-card dark>
            <v-card-title class="headline blue lighten-2">
          Un poco sobre mí
          <v-spacer/>
          <v-btn @click="$emit('cerrar')">X</v-btn>
        </v-card-title>
        <v-card-text>
            El desarrollo de software, además de mi trabajo, es una de mis grandes pasiones.
            <br>
            En mi tiempo libre, me gusta aprender nuevas tecnologías y mejorar mi metodología de trabajo
            con nuevos conceptos de clean code y patrones de diseño.
        </v-card-text>
        </v-card>
    </v-container>
</template>
<script>
export default {
    
}
</script>