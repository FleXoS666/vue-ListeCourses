<template>
  <div class="clearLink">
  <a v-if="!confirmMode" v-on:click="confirmMode=true">Vider la liste</a>
   <div v-if="confirmMode">
  <a v-on:click="mainClick">oui</a>&nbsp;
  <a v-on:click="confirmMode=false">non</a>


   </div>

  </div>
</template>

<script>
export default {
  name: 'ClearAll',
  props: {
    
  },data(){
return{
	'confirmMode': false
// 'clearList': false
}
},methods:{
mainClick(){

	this.$emit("listClearing")
this.confirmMode=false

}
}
}
</script>

<style>
a{
	/*position: absolute;*/
	background-color:red;
	color:white;
	width:7em;
	padding:0.5em;
	border-radius: 6px;
}
</style>
