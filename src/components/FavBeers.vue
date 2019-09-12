<template lang="html">
  <div>
    <ul>
      <li v-for="beer in favBeers" :beer="favBeers">{{ beer.name }}</li>
    </ul>
  </div>
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
