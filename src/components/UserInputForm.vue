<template>
	<div class="userInputForm">
		<form @submit.prevent="updateValue">
			<input class="in" type="text" name="" v-model="inputValue">
			<input class="valid" type="submit" name="" value="Ajouter">
		</form>
	</div>
</template>

<script>
	export default {
		name: 'UserInputForm',
		props: {
			
		}, data(){
			return{
				'inputValue': null,
			}
		},
		methods:{
			updateValue(){
				this.$emit("inputChanged", this.inputValue)
			}
		}
	}
</script>

<style>


</style>
