<template lang="html">
  <li v-on:click="handleClick">{{ beer.name }}</li>
</template>

<script>
import { eventBus } from '../main.js'
export default {
  name: 'list-component',
  props:['beer'],
  methods: {
    handleClick(){
      eventBus.$emit('beer-selected', this.beer)
    }
  }

}
</script>

<style lang="css" scoped>
li {
  font-family: sans-serif;
}
</style>
