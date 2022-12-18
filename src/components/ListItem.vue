<template>
    <!-- <div class="container">
      <div class="Items__wrapper" v-for="(item, index) in trips" :key="index">
        <p>{{ item.type }}</p>
        <p>{{ item.vehicle }}</p>
      </div>
    </div> -->

  <!-- <v-container>
      <v-row>
          <v-col cols="12"> -->
            <v-container>
              <v-row>
                <v-col cols="12"  v-for="(item, index) in trips" :key="index">
                  <!-- <div > -->
                    <v-row>
                      <v-col cols="12">
                        <h2 class="item__title ma-0">{{ item.name }}</h2>
                      </v-col>
                    </v-row>
                    <v-row class="d-flex justify-space-between">
                      <v-col cols="12" class="item__content-wrapper d-flex justify-space-between align-center my-5">
                        <img :src="'src/assets/' + item.image" alt="image">
                        <p class="ma-0">{{ item.stars }}</p>
                        <v-icon>{{mdiCircleSmall}}</v-icon>
                        <p class="ma-0">{{ item.type }}</p>
                        <v-icon>{{mdiCircleSmall}}</v-icon>
                        <p class="ma-0">{{ item.vehicle }}</p>
                        <v-icon>{{mdiCircleSmall}}</v-icon>
                        <p class="ma-0">{{ item.date }}</p>
                        <v-icon class="ma-0 d-md-block d-sm-none">{{mdiCircleSmall}}</v-icon>
                        <p class="ma-0 d-md-block align-items-end d-sm-none">{{ item.totalHours }}</p>
                        <v-icon v-if="item.guestsAmount" class="d-lg-block d-md-none d-sm-none">{{mdiCircleSmall}}</v-icon>
                        <p v-if="item.guestsAmount" class="ma-0 d-lg-block d-md-none d-sm-none">{{ item.guestsAmount }}</p>
                      </v-col>
                    </v-row>
                  <!-- </div> -->
                </v-col>
              </v-row>
                
            </v-container>
          <!-- </v-col>
      </v-row>
  </v-container> -->
</template>
  
  <script>
  import { mdiCircleSmall } from '@mdi/js';
  export default {
    name: "ListItem",
    data: () => ({
      mdiCircleSmall,
      // ok: "../assets/logo.png"
    }),
    // props: {
    //   msg: String,
    // },
    props: ["trips"],
  };
  </script>
  
  <!-- Add "scoped" attribute to limit CSS to this component only -->
  <style scoped>
  h3 {
    margin: 40px 0 0;
  }
  ul {
    list-style-type: none;
    padding: 0;
  }
  li {
    display: inline-block;
    margin: 0 10px;
  }
  a {
    color: #42b983;
  }
  </style>
  