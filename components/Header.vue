<template>
<div id="app">
  <client-only>
    <v-app-bar
        style="background-color: #FFB300;"
    >
        <v-toolbar-title><router-link tag="a" to="/" exact color="white">Home </router-link></v-toolbar-title>
        <v-toolbar-title><router-link tag="a" to="/restaurants">Restaurants</router-link></v-toolbar-title>
    </v-app-bar>
  </client-only>
</div>
</template>
