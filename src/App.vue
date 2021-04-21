<template>
  <v-app :style="{background: $vuetify.theme.themes.dark.background}">
    <v-app-bar :style="{background: $vuetify.theme.themes.dark.background}">
      <div class="mx-auto">
        <v-toolbar-title>Ota-Kon Titan</v-toolbar-title>
      </div>
    </v-app-bar>

      <v-main>
        <router-view></router-view>
      </v-main>

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
