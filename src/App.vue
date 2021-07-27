<template>
  <v-app>
    <v-app-bar app color="primary" dark>
      <div class="d-flex align-center">
        <v-img
          alt="Logo"
          class=" mr-2"
          contain
          src="./assets/Logo.png"
          transition="scale-transition"
          md-width="200"
          width="150"
        />
      </div>

      <v-spacer></v-spacer>

      <v-btn
      >
        <span class="mr-2">Latest Release</span>
        <v-icon>mdi-open-in-new</v-icon>
      </v-btn>
    </v-app-bar>

    <v-main>
      <MainPage/>
    </v-main>
  </v-app>
</template>

<script>
import MainPage from './views/MainPage'

export default {
  name: "App",
  components: {
    MainPage
  },
  data: () => ({
    //
  }),
};
</script>
