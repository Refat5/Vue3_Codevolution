<template>
	<div>{{ greet }} {{ name }}</div>
	<div v-text="age"></div>
	<div v-html="varsity"> </div>
	<div v-html="hack"></div>
	<div v-bind:id="headingId"> Hello V-bind Heading Id </div>
	<button v-bind:disabled="buttonDisable">Button</button>

</template>

<script>
export default {
	name: "App",
	data() {
		return {
			name: "refat",
			greet: "Hello",
			age: "45",
			varsity: "<strong>BUBT</strong>",
			hack: `<a href="#" onclick="alert('your pc is hacked ! Please give me money i will save you')">Click Hear</a>`,
			headingId: "heading",
			buttonDisable: false,
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
