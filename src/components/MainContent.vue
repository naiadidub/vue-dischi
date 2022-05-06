<template>
  <div class="container">
    <div class="row">
      <DiscCard/>
    </div>
  </div>
</template>

<script>
import axios from 'axios'
import DiscCard from './DiscCard.vue'

export default {
  name: 'MainContent',
  components: {
    DiscCard
  },
  data(){
    return{
      DiscLIst: []
    } 
  },
  created(){
    axios.get('https://flynn.boolean.careers/exercises/api/array/music').then((res)=>{
      this.DiscLIst = res.data.response
      console.log(this.DiscLIst)
    })
  }
  
}
</script>


<style scoped lang="scss">

</style>
