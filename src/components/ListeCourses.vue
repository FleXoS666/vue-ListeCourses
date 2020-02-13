<template>
  <div class="hello">
  
    <ul >
      <li v-for="(itemList,index) in itemsList" :key='index' :value="index">{{ itemList }}</li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'ListeCourses',
  props: {
    inputValue:String,
    itemsList: Array
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
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
