<template>
  <div class="clearLink">
  <a v-on:click="clearList">Vider la liste</a>
   
  </div>
</template>

<script>
export default {
  name: 'ClearAll',
  props: {
    
  },data(){
return{
// 'clearList': false
}
},methods:{
clearList(){

this.$emit("listClearing")
}
}
}
</script>

<style>
.clearLink{
	position: absolute;
	background-color:red;
	color:white;
	width:7em;
	margin-left:1em;
	padding:0.5em;
	border-radius: 6px;
}
</style>
