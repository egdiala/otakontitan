<template>
  <v-app :style="{background: $vuetify.theme.themes.dark.background}">
    <v-app-bar style="display: none;"></v-app-bar>

    <v-main>
      <HelloWorld/>
    </v-main>

      <v-bottom-navigation app shift color="yellow" background-color="background">
    <v-btn>
      <span>Home</span>
      <v-icon>mdi-home</v-icon>
    </v-btn>

    <v-btn>
      <span>Booking</span>
      <v-icon>mdi-account-cash</v-icon>
    </v-btn>

    <v-btn>
      <span>Gallery</span>
      <v-icon>mdi-file-image</v-icon>
    </v-btn>
  </v-bottom-navigation>
  </v-app>
</template>

<script>
import HelloWorld from './components/HelloWorld';

export default {
  name: 'App',

  components: {
    HelloWorld,
  },

  data: () => ({
    active: true,
    value: 'home'
  }),

  mounted() {
    this.$vuetify.theme.dark = true;
  },
};
</script>
