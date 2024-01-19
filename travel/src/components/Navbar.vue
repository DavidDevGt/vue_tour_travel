<template>
  <v-app-bar height="80" color="#FEF5F8" scroll-behavior="elevate" id="inspire">
    <v-img class="" src="/1.png"></v-img>
    <v-spacer></v-spacer>
    <v-menu transition="slide-x-transition">
      <template v-slot:activator="{ props }">
        <v-btn color="#165EA5" v-bind="props">Home +</v-btn>
      </template>
      <v-list>
        <v-list-item>
          <v-list-item-title>Home Page One</v-list-item-title>
          <v-list-item-title>Home Page Two</v-list-item-title>
        </v-list-item>
      </v-list>
    </v-menu>

    <v-menu transition="slide-x-transition">
      <template v-slot:activator="{ props }">
        <v-btn color="#165EA5" v-bind="props">Tours +</v-btn>
      </template>
      <v-list>
        <v-list-item>
          <v-list-item-title>Tout Grid</v-list-item-title>
          <v-list-item-title>Tour List</v-list-item-title>
          <v-list-item-title>Tour Single</v-list-item-title>
        </v-list-item>
      </v-list>
    </v-menu>

    <v-menu transition="slide-x-transition">
      <template v-slot:activator="{ props }">
        <v-btn color="#165EA5" v-bind="props">Hotel</v-btn>
      </template>
    </v-menu>

    <v-menu transition="slide-x-transition">
      <template v-slot:activator="{ props }">
        <v-btn color="#165EA5" v-bind="props">Pages +</v-btn>
      </template>
      <v-list>
        <v-list-item>
          <v-list-item-title>About</v-list-item-title>
          <v-list-item-title>Team</v-list-item-title>
          <v-list-item-title>FAQ</v-list-item-title>
          <v-list-item-title>404</v-list-item-title>
        </v-list-item>
      </v-list>
    </v-menu>

    <v-menu transition="slide-x-transition">
      <template v-slot:activator="{ props }">
        <v-btn color="#165EA5" v-bind="props">Blog</v-btn>
      </template>
    </v-menu>

    <v-menu transition="slide-x-transition">
      <template v-slot:activator="{ props }">
        <v-btn color="#165EA5" v-bind="props">Contact</v-btn>
      </template>
    </v-menu>
    <v-btn
      class="text-none expl mr-8 animate__animated"
      @mouseover="animateButton"
      color="indigo-lighten-1"
      style="scale: 0.9; font-weight: bold"
      size="x-large"
      variant="flat"
      rounded="0"
    >
      Get Started
    </v-btn>
  </v-app-bar>
</template>

<script>
export default {
  methods: {
    animateButton(event) {
      // Agrega la clase de animación cuando el ratón pasa por encima del botón
      event.target.classList.add("animate__headShake");
    },
  },
};
</script>

<style scope>
.expl {
  background-color: white;
  color: #165ea5;
}
</style>
