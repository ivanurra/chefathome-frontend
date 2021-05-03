<template>
  <div>
    <v-form>
      <v-text-field
        v-model="query"
        background-color="white"
        color="black"
        label="Search restaurants"
        placeholder="Search restaurants"
      ></v-text-field>
    </v-form>
    <v-card v-for="restaurant in filteredList" v-bind:key="restaurant">
      <div>
        <img :src="'http://localhost:1337/' + restaurant.image.url" alt="" />
        <canvas width="300" height="200"></canvas>
      </div>
      <div>
        <div>
          <h3>{{ restaurant.name }}</h3>
          <p>{{ restaurant.description }}</p>
          <router-link
            :to="{ name: 'restaurants-id', params: { id: restaurant.id } }"
            tag="a"
          >
            See dishes
          </router-link>
        </div>
      </div>
    </v-card>
    <div v-if="filteredList.length == 0">
      <p>No restaurants found</p>
    </div>
  </div>
</template>

<script>
// Import the restaurants query
import restaurantsQuery from '~/apollo/queries/restaurant/restaurants'

export default {
  data() {
    return {
      // Initialize an empty restaurants variabkle
      restaurants: [],
      query: '',
    }
  },
  apollo: {
    restaurants: {
      prefetch: true,
      query: restaurantsQuery,
    },
  },
  computed: {
    // Search system
    filteredList() {
      return this.restaurants.filter((restaurant) => {
        return restaurant.name.toLowerCase().includes(this.query.toLowerCase())
      })
    },
  },
}
</script>