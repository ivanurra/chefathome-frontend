<template>
  <v-app-bar style="background-color: rgb(243, 162, 44)" max-height="60px">
    <v-tab
      ><router-link tag="a" to="/" style="text-decoration: none; color: black"
        ><strong>CHEF AT HOME</strong></router-link
      ></v-tab
    >
    <v-tab
      ><router-link
        tag="a"
        to="/restaurants"
        style="text-decoration: none; color: black"
        ><strong>Restaurants</strong></router-link
      ></v-tab
    >
  </v-app-bar>
</template>
