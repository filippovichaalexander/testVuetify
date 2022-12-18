<template>
  <v-app>
    
    <!-- <v-app-bar
      app
      color="primary"
      dark
    >
      <div class="d-flex align-center">
        <v-img
          alt="Vuetify Logo"
          class="shrink mr-2"
          contain
          src="https://cdn.vuetifyjs.com/images/logos/vuetify-logo-dark.png"
          transition="scale-transition"
          width="40"
        />

        <v-img
          alt="Vuetify Name"
          class="shrink mt-1 hidden-sm-and-down"
          contain
          min-width="100"
          src="https://cdn.vuetifyjs.com/images/logos/vuetify-name-dark.png"
          width="100"
        />
      </div>

      <v-spacer></v-spacer>

      <v-btn
        href="https://github.com/vuetifyjs/vuetify/releases/latest"
        target="_blank"
        text
      >
        <span class="mr-2">Latest Release</span>
        <v-icon>mdi-open-in-new</v-icon>
      </v-btn>
    </v-app-bar> -->

    <v-main>
      <ListItems :trips="trips"/>
    </v-main>
  </v-app>
</template>

<script>
import ListItems from "./components/ListItems.vue";

export default {
  name: 'App',
    data() {
      return {
        trips: [
          {
            name: '"Город сыра и мира"',
            stars: 5,
            type: "Историческая",
            vehicle: "На автобусе",
            date: "28 марта",
            totalHours: "9 часов",
            image: "logo.png"
          },
          {
            name: 'Экскурсия в национальный парк "Куршская коса"',
            stars: 5,
            type: "Обзорная",
            vehicle: "На автобусе",
            date: "25 марта",
            totalHours: "6 часов",
            image: "../assets/star.png"
          },
          {
            name: '"О кирхах, рыцарях и замках"',
            stars: 5,
            type: "Историческая",
            vehicle: "На автобусе",
            date: "29 марта",
            totalHours: "6 часов",
          },
          {
            name: "Экскурсия в Янтарный",
            stars: 4,
            type: "Историческая",
            vehicle: "На автобусе",
            date: "29 марта",
            totalHours: "6 часов",
            guestsAmount: "до 49",
          },
        ],
      };
    },


  components: {
    ListItems
  },
};
</script>
