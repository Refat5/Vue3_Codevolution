<template>
	<div>{{ greet }} {{ name }}</div>
	<div v-text="age"></div>
</template>

<script>
export default {
	name: "App",
	data() {
		return {
			name: "refat",
			greet: "Hello",
			age: "45",
		};
	},
};
</script>

<style>
#app {
	font-family: Avenir, Helvetica, Arial, sans-serif;
	-webkit-font-smoothing: antialiased;
	-moz-osx-font-smoothing: grayscale;
	text-align: center;
	color: #2c3e50;
	margin-top: 60px;
}
</style>
