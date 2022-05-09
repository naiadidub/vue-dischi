<template>
  <div id="app">

    <HeaderContent :Lista="DiscLIst"/>
    <MainContent :Lista="DiscLIst"/>
  </div>
</template>

<script>
import axios from 'axios'
import MainContent from './components/MainContent.vue'
import HeaderContent from './components/HeaderContent.vue'

export default {
  name: 'App',
  components: {
    MainContent,
    HeaderContent,
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

<style lang="scss">
@import './styles/variables.scss';
#app{
  background-color: $bgblue;
}
</style>
