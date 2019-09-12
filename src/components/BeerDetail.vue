<template lang="html">
  <article v-if="beer">
    <p><span>Beer Details</span>: {{ beer.name }}</p>
    <p><span>Food Pairing</span>:</p>
    <ol>
      <li>{{ beer.food_pairing[0] }}</li>
      <li>{{ beer.food_pairing[1] }}</li>
      <li>{{ beer.food_pairing[2] }}</li>
    </ol>
    <p><img :src="beer.image_url" style="width:30%; height:30%"/></p>
  </article>
</template>

<script>
export default {
  name: 'beer-detail',
  props: ['beer']
}
</script>

<style lang="css" scoped>


</style>
