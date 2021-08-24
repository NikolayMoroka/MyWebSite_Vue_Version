<template>
  <v-container>
    <v-row class="text-center">
      <v-col cols="12">
        <Welcome/>
      </v-col>
      <v-col cols="12">
        <InfoBlock/>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
import Welcome from "./Welcome.vue"
import InfoBlock from "./InfoBlock.vue"

export default {
  name: "MainPage",
  components: {
    Welcome,
    InfoBlock
  },
  data: () => ({
    
    
   
  }),
};
</script>

<style scoped>

</style>
