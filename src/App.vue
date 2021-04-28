<template>
  <v-app :style="{background: $vuetify.theme.themes.dark.background}">
    <v-app-bar v-if="!isMobile" app fixed color="background">
        <v-img src="@/assets/logo.png" max-height="50" max-width="100" contain></v-img>
        
        <div class="mx-auto">
        <v-btn text plain :ripple="false" :to="{ path: '/' }">
            <span>Home</span>
        </v-btn>

        <v-btn text plain :ripple="false" :to="{ path: '/booking' }">
            <span>Booking</span>
        </v-btn>

        <v-btn text plain :ripple="false" :to="{ path: '/gallery' }">
            <span>Gallery</span>
        </v-btn>
        </div>
    </v-app-bar>
    <v-app-bar v-else
      :collapse="!collapseOnScroll"
      :collapse-on-scroll="collapseOnScroll" app fixed color="background">
        <v-icon @click="overlay = !overlay" size="1.5x" class="custom-class mx-auto">mdi-menu</v-icon>
        <v-spacer></v-spacer>
        <v-img src="@/assets/logo.png" max-height="50" max-width="50" contain></v-img>
    </v-app-bar>

      <v-main>
        <router-view></router-view>
          <v-footer padless>
            <v-col
              class="text-center"
              cols="12"
            >
              {{ new Date().getFullYear() }} | <strong>LeatherWorks Media</strong> - <a href="https://twitter.com/e_diala?s=09" target="_blank">👨🏾‍💻</a> & <a href="https://twitter.com/tobecci?s=08" target="_blank">👨🏾‍💻</a> 
            </v-col>
          </v-footer>
      </v-main>
 <v-overlay :opacity="opacity" :value="overlay">
       <v-icon @click="overlay = false" size="1.5x" class="custom-class" style="position: fixed; top: 4%; right: 1.5em; z-index: 99999;">mdi-window-close</v-icon>
       <v-row class="text-center">
         <v-col cols="12">
            <v-btn text plain :ripple="false" :to="{ path: '/' }" @click="overlay = false">
            <span>Home</span>
        </v-btn></v-col>
         <v-col cols="12">
        <v-btn text plain :ripple="false" :to="{ path: '/booking' }" @click="overlay = false">
            <span>Booking</span>
        </v-btn></v-col>
         <v-col cols="12">
        <v-btn text plain :ripple="false" :to="{ path: '/gallery' }" @click="overlay = false">
            <span>Gallery</span>
        </v-btn></v-col>
       </v-row>
    </v-overlay>
  </v-app>
</template>

<script>
export default {
  name: 'App',
  data: () => ({
    collapseOnScroll: true,
    opacity: 0.9,
    overlay: false,
  }),
  computed: {
    isMobile(){
      const isMobile = /iPhone|iPad|iPod|Android/i.test(navigator.userAgent);
      return isMobile;
    },
  },
  mounted() {
    this.$vuetify.theme.dark = true;
  },
};
</script>
