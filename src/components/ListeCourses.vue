<template>
  <div class="hello">
    <!-- <p v-if="itemsList=[]">Rien</p> -->
    <ul>
      <li v-for="(itemList,index) in itemsList" :key='index' :value="index">{{ itemList }}  <button v-on:click="delElmt(index)">X</button></li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'ListeCourses',
  props: {
    inputValue:String,
    itemsList: Array,
    clearList: Boolean,
  },methods:{
    delElmt(index){
      console.log(index)
      this.$emit("deleteElement", index)
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style >
h3 {
  margin: 40px 0 0;
}
ul {
  margin: 4em;
  list-style-type: none;
  padding: 0;
  border:1px solid black;
  border-radius: 6px;
}
li {
  border:2px solid green;
  margin: 10px;
  padding: 0.3em;
}
</style>
