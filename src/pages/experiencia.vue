<template>
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
</template>
<script>
export default {
    
}
</script>