<template>
  <v-container fluid>
    <v-row align="center" justify="center">
      <v-col cols="12" md="5" align="center" justify="center">
        <v-img
          src="logomain.png"
          alt="Chef at home logo"
          max-width="550px"
          max-height="334.40px"
        />
        <h2 class="font-italic font-weight-light black--text">
          We deliver the best food in the world to your door.
        </h2>
      </v-col>
      <v-col cols="12" md="7" align="center" justify="center">
        <v-carousel
          cycle
          :height="$vuetify.breakpoint.xs ? '300px' : '1000px'"
          hide-delimiter-background
          hide-delimiter
          :show-arrows="false"
        >
          <v-carousel-item
            v-for="(item,i) in items"
            :key="i"
            :src="item.src"
            reverse-transition="fade-transition"
            transition="fade-transition"
          ></v-carousel-item>
        </v-carousel>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
  export default {
    data () {
      return {
        items: [
          {
            src: 'foodmain1.jpg',
          },
          {
            src: 'foodmain2.jpg',
          },
          {
            src: 'foodmain3.jpg',
          },
          {
            src: 'foodmain4.jpg',
          },
        ],
      }
    },
  }
</script>