<template>
  <div class="container">
    
    <div class="row">
      <DiscCard v-for="(disc, index) in Lista" :key="index"
      :SrcImage="disc.poster"
      :Tytle="disc.title"
      :Author="disc.author"
      :Year="disc.year"
      />
    </div>
  </div>
</template>

<script>

import DiscCard from './DiscCard.vue'


export default {
  name: 'MainContent',
  components: {
    DiscCard,
  },
  props:{
    Lista: Array
  }
} 

</script>


<style scoped lang="scss">

</style>
