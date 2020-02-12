<template>
  <div id="app">
    <!-- <img alt="Vue logo" src="./assets/logo.png"> -->
    <Top :title="title"></Top>
    <ListeCourses msg="Welcome to Your Vue.js App"/>
  </div>
</template>

<script>
import ListeCourses from './components/ListeCourses.vue'
import Top from './components/Top.vue'

export default {
  name: 'App',
  components: {
    ListeCourses,
    Top
  },
  data(){
    return{
      'title': "Liste de courses",
    }
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  
}
</style>
