<template>
	<div>{{ greet }} {{ name }}</div>
	<div v-text="age"></div>
	<div v-html="varsity"> </div>
	<div v-html="hack"></div>
	<div v-bind:id="headingId"> Hello V-bind Heading Id </div>
	<button v-bind:disabled="buttonDisable">Button</button>
	<div class="underline">Underline</div>
	<div class="underline" v-bind:class="status"> Status</div>
	<hr>
	<h3 v-bind:class="isPromoted">This movie is Promoted</h3>

	<h4 v-bind:class="isSoldOut ? 'soldOut' : 'notSoldOut' ">The Movie Sold Out </h4>

	<h3 v-bind:class="['notSoldOut', 'promoted']"> Newly Promoted movie</h3>

	<h2 v-bind:class="[isPromoted && 'promoted', isSoldOut ? 'soldOut' : 'notSoldOut']"> Array Conditional Class binding</h2>

	<h2 v-bind:class="{
        promoted:isPromoted,
          soldOut:isSoldOut
    }"> Object Conditional Class binding</h2>

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
			status: "text-danger",
			isPromoted: false,
			isSoldOut: true,
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
.underline {
	text-decoration: underline;
	font-size: 50px;
}
.promoted {
	font-family: inherit;
	font-style: italic;
}
.soldOut {
	color: rgb(221, 14, 14);
}
.notSoldOut {
	color: rgb(28, 165, 28);
}
</style>
