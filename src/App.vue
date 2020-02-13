<template>
  <div id="app">
    <!-- <img alt="Vue logo" src="./assets/logo.png"> -->
    <Top :title="title"></Top>
    <UserInputForm @inputChanged="updateList"></UserInputForm>
    <ClearAll @listClearing="clearList"></ClearAll>
    <ListeCourses :itemsList="itemsList" @deleteElement="delElmt"/>
    
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
      'itemsList': [],

    }
  },mounted(){
console.log('essayes de recuperer la liste')
      localStorage.getItem(this.itemsList)
      // console.log(this.List)
      console.log(this.itemsList)
      console.log("mais")
  }


  ,methods:{
    itemsListing(){
localStorage.getItem(this.itemsList)
    },
    updateList(newItem){
      this.itemsList.push(newItem)
      localStorage.setItem(newItem, this.itemsList)
    },
    clearList(){
    this.itemsList=[]
        // this.itemsList.clear()
    },
    delElmt(itemKey){
    // this.itemsList.splice(itemKey,1)
    localStorage.removeItem(this.itemsList.splice(itemKey,1))
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
