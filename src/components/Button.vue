<template>
	<button @click="onClick()" class="btn" :style="{ background: color }">{{text}}</button>
</template>

<script>
export default {
	name: "ButtonComponent",
	props: {
		text: String,
		color: String,
	},
	methods: {
		onClick() {
			console.log("Button clicked")
		}
	},
}
</script>