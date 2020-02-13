<template>
  <div class="userInputForm">
    <form>
    <input class="in" type="text" name="" v-model="inputValue">
    <input class="valid" type="submit" name="" value="Ajouter">
    </form>
  </div>
</template>

<script>
export default {
  name: 'UserInputForm',
  props: {
    "inputValue":null,
  }
}
</script>

<style>
form{
	border:1px solid black;
	margin: 1em;
	padding: 0.3em;
	background-color: #3EB650
}
input{
	margin: 0.5em;
}
.in{
	height:2em;

}
.valid{
	height:1.5em;
	width: 5em;
	background-color: red;
	color: white
}


</style>
