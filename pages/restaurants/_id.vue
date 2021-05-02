<template>
<div>

  // Link to go back to the previous page
  <a @click="$router.go(-1)">go back</a>

  <client-only>
  <div>

      // Left card displaying dishes
      <div >
        <div v-for="dish in restaurant.dishes">
            <div >
                <div >
                    <img :src="'http://localhost:1337/' + dish.image.url" alt="" width="300px"/>
                </div>
                <div>
                    <h3>{{ dish.name }} {{ dish.price }}€</h3>
                    <p>{{ dish.description }}</p>
                </div>
                <div>
                  // Doing nothing for the moment :)
                  <button>Add to cart</button>
                </div>
            </div>
        </div>
      </div>

      // Right card that will display your cart
      <div>
      </div>

  </div>

  </client-only>
</div>
</template>

<script>
import restaurantQuery from '~/apollo/queries/restaurant/restaurant'

export default {
  data() {
    return {
      restaurant: Object
    }
  },
  apollo: {
    restaurant: {
      prefetch: true,
      query: restaurantQuery,
      variables () {
        return { id: this.$route.params.id }
      }
    }
  }
}
</script>