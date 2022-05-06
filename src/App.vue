<template>
  <div id="app">
    <HeaderContent/>
    <MainContent/>
  </div>
</template>

<script>

import MainContent from './components/MainContent.vue'
import HeaderContent from './components/HeaderContent.vue'

export default {
  name: 'App',
  components: {
    MainContent,
    HeaderContent
  }
}
</script>

<style lang="scss">

@import './styles/variables.scss';
#app{
  background-color: $bgblue;
}
</style>
