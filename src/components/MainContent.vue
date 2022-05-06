<template>
  <div class="container">
    <LoaderComponent v-if="Loading"/>
    <div class="row">
      <DiscCard v-for="(disc, index) in DiscLIst" :key="index"
      :SrcImage="disc.poster"
      :Tytle="disc.title"
      :Author="disc.author"
      :Year="disc.year"
      />
    </div>
  </div>
</template>

<script>
import axios from 'axios'
import DiscCard from './DiscCard.vue'
import LoaderComponent from './LoaderComponent.vue'

export default {
  name: 'MainContent',
  components: {
    DiscCard,
    LoaderComponent
  },
  data(){
    return{
      DiscLIst: [],
      Loading: false
    } 
  },
  created(){
    this.loading = true
    axios.get('https://flynn.boolean.careers/exercises/api/array/music').then((res)=>{
      this.DiscLIst = res.data.response
      this.loading = false
      console.log(this.DiscLIst)
    })
  }
  
}
</script>


<style scoped lang="scss">

</style>
