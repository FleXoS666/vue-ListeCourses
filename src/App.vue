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
      'itemsList': ["bite","chatte"],

    }
  },mounted(){
// localStorage
  }


  ,methods:{
    updateList(newItem){
      this.itemsList.push(newItem)
      console.log(this.itemsList.slice(2,3));
    },
    clearList(){
    this.itemsList=[]
        // this.itemsList.clear()
    },
    delElmt(itemKey){
     
      // var itemKey2=parseFloat(itemKey) +1
    this.itemsList.splice(itemKey,1)
 // console.log(itemKey,itemKey2)
// this.itemsList.delete(Elt)
// console.log(Elt)
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
