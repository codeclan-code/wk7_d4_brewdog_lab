<template lang="html">
  <article v-if="beer">
    <div>
      <button v-on:click="saveToFav">Add to Favourites</button>
    </div>
    <h1><span><strong>Beer Details</strong></span>: {{ beer.name }} </h1>
    <p><span><strong>Food Pairing</strong></span>:</p>
    <ol>
      <li>{{ beer.food_pairing[0] }}</li>
      <li>{{ beer.food_pairing[1] }}</li>
      <li>{{ beer.food_pairing[2] }}</li>
    </ol>
    <p><img :src="beer.image_url" style="width:30%; height:30%"/></p>
  </article>
</template>

<script>
import { eventBus } from '../main.js'
export default {
  name: 'beer-detail',
  props: ['beer'],
  methods: {
    saveToFav(){
      eventBus.$emit('beer-selected', this.beer);
      favBeers.push(this.selectedBeer)
    }
  }
}
</script>

<style lang="css" scoped>


</style>
