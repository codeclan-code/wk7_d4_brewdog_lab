<template lang="html">
  <article v-if="beer">
  <p><span>Beer Name</span>: {{ beer.name }}</p>
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
