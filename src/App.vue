<template>
  <div id="app">
    <!-- <img alt="Vue logo" src="./assets/logo.png"> -->
    <Top :title="title"></Top>
    <UserInputForm @inputChanged="updateList"></UserInputForm>
    <ClearAll></ClearAll>
    <ListeCourses :itemsList="itemsList"/>
    
  </div>
</template>

<script>
import ListeCourses from './components/ListeCourses.vue'
import Top from './components/Top.vue'
import UserInputForm from './components/UserInputForm.vue'
import ClearAll from './components/ClearAll.vue'

export default {
  name: 'App',
  components: {
    ListeCourses,
    Top,
    UserInputForm,
    ClearAll,
  },
  data(){
    return{
      'title': "Liste de courses",
      'itemsList': ["bite","chatte"],

    }
  },methods:{
    updateList(newItem){
      this.itemsList.push(newItem)
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
