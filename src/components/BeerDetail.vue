<template lang="html">
<article>
  <p><span>Beer Name</span>: {{beer.name}}</p>
</article>
</div>
</template>

<script>
export default {
  name: 'beer-detail',
  props: ['beer']
}
</script>

<style lang="css" scoped>
</style>
