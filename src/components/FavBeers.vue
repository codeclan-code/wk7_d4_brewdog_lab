<template lang="html">
  <ul>
    <li v-for="beer in favBeers" :beer="favBeers">{{ beer.name }}</li>
  </ul>
</template>

<script>
import { eventBus } from '../main.js'
export default {
  name: 'fav-beers',
  props: ['favBeers']
}
</script>

<style lang="css" scoped>
</style>
