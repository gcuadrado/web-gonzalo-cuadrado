<template>
    <v-container>
        <v-img :src="source"/>
    </v-container>
</template>
<script>
export default {
    props:{
        source: String
    }
}
</script>