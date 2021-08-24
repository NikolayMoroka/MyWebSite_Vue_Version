<template>
  <v-app class="app">
      <v-app-bar app color="#290653" dark large>
        <div style="width: 100%" class="d-flex align-center justify-space-between">
          <div>
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
          <v-app-bar-nav-icon @click="drawer = true"></v-app-bar-nav-icon>
        </div>
        <v-spacer></v-spacer>
      </v-app-bar>
    
      <v-navigation-drawer
      v-model="drawer"
      absolute
      temporary
      width="100%"
      height="30vh"
    >
      <v-list
        nav
        dense
      >
        <v-list-item-group
          v-model="group"
          active-class="deep-purple--text text--accent-4"
          class="text-center"
        >
          <v-list-item>
            <v-list-item-icon>
              <v-icon>mdi-home</v-icon>
            </v-list-item-icon>
            <v-list-item-title>Home</v-list-item-title>
          </v-list-item>

          <v-list-item>
            <v-list-item-icon>
              <v-icon>mdi-account</v-icon>
            </v-list-item-icon>
            <v-list-item-title>Account</v-list-item-title>
          </v-list-item>
        </v-list-item-group>
      </v-list>
    </v-navigation-drawer>


    

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
    MainPage,
  },
  data: () => ({
    drawer: false,
    group: null,
  }),
};
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=PT+Sans:wght@400;700&display=swap');
  .app {
    background-color: #3f0a7c !important;
  }

  /* style for animation */

/* .animation_backInLeft {
  animation: backInLeft;
  animation-duration: 2.5s;
}

.animation_backInRight {
  animation: backInRight;
  animation-duration: 2.5s;
}

.animation_backInUp {
  animation: fadeInUpBig;
  animation-duration: 2.5s;
}

[data-aos="rotate"] {
  transform: rotate(-360deg);
  opacity: 0;
}

[data-aos="rotate"].aos-animate {
  transform: rotate(0);
  opacity: 1;
}

[data-aos="tracking-in-contract"] {
  letter-spacing: 1em;
  opacity: 0;
}

[data-aos="tracking-in-contract"].aos-animate {
  letter-spacing: normal;
  opacity: 1
} */
</style>
