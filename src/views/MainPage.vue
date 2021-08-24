<template>
  <v-container>
    <v-btn
      v-scroll="onScroll"
      v-show="fab"
      fab
      dark
      fixed
      bottom
      right
      style="border-color: rgb(63, 10, 124);"
      color="#ffffff5c"
      @click="toTop"
    >
      <v-icon x-large color="#3f0a7c">mdi-chevron-up</v-icon>
    </v-btn>
    <v-row class="text-center">
      <v-col cols="12">
        <Welcome/>
      </v-col>
      <v-col cols="12">
        <InfoBlock/>
      </v-col>
      <v-col cols="12">
        <Contacts/>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
import Welcome from "./Welcome.vue"
import InfoBlock from "./InfoBlock.vue"
import Contacts from "./Contacts.vue"

export default {
  name: "MainPage",
  components: {
    Welcome,
    InfoBlock,
    Contacts
  },
  data: () => ({
    fab: false,
  }),

  methods: {
    onScroll (e) {
      if (typeof window === 'undefined') return
      const top = window.pageYOffset ||   e.target.scrollTop || 0
      this.fab = top > 20
    },
    toTop () {
      this.$vuetify.goTo(0)
    }
  }
};
</script>

<style scoped>

</style>
