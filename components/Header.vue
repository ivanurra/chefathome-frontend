<template>
<div id="app">
  <client-only>
    <v-app-bar
        style="background-color: #FFB300;"
        dense
    >
        <v-tab><router-link tag="a" to="/" style="text-decoration: none; color: black;">CHEF AT HOME</router-link></v-tab>
        <v-tab><router-link tag="a" to="/restaurants" style="text-decoration: none; color: black;">Restaurants</router-link></v-tab>
    </v-app-bar>
  </client-only>
</div>
</template>
