<template>
    <v-footer dark :app="$vuetify.breakpoint.mdAndUp" :absolute="$vuetify.breakpoint.mdAndUp">
      <v-container class="d-flex">
        <v-col align="center">
          {{ new Date().getFullYear() }} (C)<strong> Iván Urra</strong>
        </v-col>
      </v-container>
    </v-footer>
</template>