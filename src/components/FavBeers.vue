<template lang="html">
  <div>
    <ul>
      <h2>Favorite Beers</h2>
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
ul {
  list-style: none;
  border: 1px solid navy;
  width: 200px;
  height: auto;
  padding: 10px;
  padding-top:0px;
  margin-top: 0px;
  margin-right:20px;
  font-weight: normal;
  border-radius: 10px;
  background-color: #B7E0DC;

}
li {
  padding:5px;

}
</style>
