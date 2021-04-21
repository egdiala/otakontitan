<template>
  <div class="home">
    <v-img
  lazy-src="https://picsum.photos/id/11/10/6"
  aspect-ratio="1"  max-height="400"
  src="@/assets/otakontitan-hero.jpeg"
></v-img>
    <v-container>
    <v-row class="text-center">
      <v-col cols="12" xl="12" lg="12" md="12" sm="12" class="mb-4">
        <h1 class="display-1 font-weight-bold mb-3">
          Coming Up Soon!!
        </h1>

        <p class="subheading font-weight-regular">
          For all those who love
          <br>Naruto, Demon Slayer, Attack on Titan, One Piece, JoJo's Bizarre Adventures and other anime, <br>
          there will be a lot of fun stuffs like... 
        </p>
      </v-col>

      <v-col
        class="mb-5 mx-auto"
        cols="12" xl="7" lg="7" md="7" sm="10" 
      >
        <div>
          <h2 class="headline font-weight-bold mb-3">
            Pool Party
          </h2>
          <p class="subheading font-weight-regular">
            There'll be a pool available at the venue for y'all to swim (hopefully not drown) and knock yourselves out. 🙂 
          </p>        
        </div>
        <v-carousel cycle hide-delimiters>
          <v-carousel-item
            v-for="(pool,i) in pools"
            :key="i"
            :src="require(`../assets/${pool.src}`)"
          ></v-carousel-item>
        </v-carousel>
      </v-col>
    </v-row>
    <v-row class="text-center">
      <v-col
        class="mb-5 mx-auto"
        cols="12" xl="7" lg="7" md="7" sm="10" 
      >
        <div>
          <h2 class="headline font-weight-bold mb-3">
            Indoor & Outdoor Games
          </h2>
          <p class="subheading font-weight-regular">
            There'll be video games available along with board games and other fun stuff for y'all. 🙂 
          </p>        
        </div>
        <v-carousel cycle hide-delimiters>
          <v-carousel-item
            v-for="(game,i) in games"
            :key="i"
            :src="require(`../assets/${game.src}`)"
          ></v-carousel-item>
        </v-carousel>
      </v-col>
    </v-row>
    <v-row class="text-center">
      <v-col
        class="mb-5 mx-auto"
        cols="12" xl="7" lg="7" md="7" sm="10" 
      >
        <div>
          <h2 class="headline font-weight-bold mb-3">
            Food & Drinks
          </h2>
          <p class="subheading font-weight-regular">
            We have registered food vendors ready to serve you and sell to you on that day. There'll be a lot to eat and drink. 🙂 
          </p>        
        </div>
        <v-carousel cycle hide-delimiters>
          <v-carousel-item
            v-for="(food,i) in foods"
            :key="i"
            :src="require(`../assets/${food.src}`)"
          ></v-carousel-item>
        </v-carousel>
      </v-col>
    </v-row>
    <v-row class="text-center">
      <v-col
        class="mb-5 mx-auto"
        cols="12" xl="7" lg="7" md="7" sm="10" 
      >
        <div>
          <h2 class="headline font-weight-bold mb-3">
            Other Events
          </h2>
          <p class="subheading font-weight-regular">
            Anime booth - OST Sing along - Guess the OST - Pool volley ball - snooker - Board games - Cosplay and lots more 
          </p>        
        </div>
      </v-col>
    </v-row>
    </v-container>
  </div>
</template>

<script>
  export default {
    name: 'Home',

    data: () => ({
      pools: [{
        src: 'pool1.jpg',
      },{
        src: 'pool2.jpg',
      },{
        src: 'pool3.png',
      }],
      games: [{
        src: 'games2.png',
      },{
        src: 'games3.jpeg',
      },{
        src: 'games1.jpg',
      }],
      foods: [{
        src: 'food2.jpg',
      },{
        src: 'food3.gif',
      },{
        src: 'food1.jpg',
      }],
    }),
  }
</script>
