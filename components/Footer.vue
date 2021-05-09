<template>
  <v-footer
    :app="$vuetify.breakpoint.mdAndUp"
    :absolute="$vuetify.breakpoint.mdAndUp"
  >
    <v-container class="d-flex">
      <v-col align="center">
        {{ new Date().getFullYear() }} (c)<strong> Chef at Home.</strong> Made by Iván Urra
      </v-col>
    </v-container>
  </v-footer>
</template>