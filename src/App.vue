<template>
  <v-app :style="{background: $vuetify.theme.themes.dark.background}">
    <v-app-bar dense color="background" style="display: none;">
        <v-toolbar-title class="mx-auto">Ota-Kon Titan</v-toolbar-title>
    </v-app-bar>

      <v-main>
        <router-view></router-view>
    <v-bottom-navigation app shift color="yellow" background-color="background">
        <v-btn :to="{ path: '/' }">
            <span>Home</span>
            <v-icon>mdi-home</v-icon>
        </v-btn>

        <v-btn :to="{ path: '/booking' }">
            <span>Booking</span>
            <v-icon>mdi-account-cash</v-icon>
        </v-btn>

        <v-btn :to="{ path: '/gallery' }">
            <span>Gallery</span>
            <v-icon>mdi-file-image</v-icon>
        </v-btn>
  </v-bottom-navigation>
      </v-main>

  </v-app>
</template>

<script>
export default {
  name: 'App',

  data: () => ({

  }),

  mounted() {
    this.$vuetify.theme.dark = true;
  },
};
</script>
