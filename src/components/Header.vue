<template>
	<header>
		<h1>{{title}}</h1>
		<ButtonComponent text="Add text" color="green" />
	</header> 
</template>

<script>
import ButtonComponent from './Button'

export default {
	name: "HeaderComponent",
	props: {
		title: {
			type: String,
			default: "No title given"
		}
	},
	components: {
		ButtonComponent
	}
}
</script>

<style scoped>
	header {
		display: flex;
		justify-content: space-between;
		align-items: center;
		margin-bottom: 20px;

	}
</style>