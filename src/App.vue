<template>
	<!-- <div>{{ greet }} {{ name }}</div>
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

	<h2 :class="{
        promoted:isPromoted,
          soldOut:isSoldOut
    }"> Object Conditional Class binding  V-bind short with just :sd</h2>

	<h3 v-bind:style="{
        color:highlightColor,
        fontSize:headerSize + 'px',
        padding:'20px',
    }">In line Style</h3>

	<h2 v-bind:style="h2StyleObject">
		Object Style
	</h2>

	<h3 v-bind:style="[baseStyleObject,successStyleObject]">Array Base Bind Style</h3>
	<h3 v-bind:style="[baseStyleObject,dangerStyleObject]">Array Base Bind Style</h3> -->

	<h3 v-if="number === 0"> The Number is 07 </h3>
	<h3 v-else-if="number < 0"> The Number is Negative </h3>

	<h3 v-else-if="number > 0"> The Number is Positive </h3>
	<h3 v-else> This is not a number </h3>

	<div v-if="number == 'hello'">
		<h4>HI</h4>
		<h4>Refat</h4>
		<h4>Whats Up</h4>
	</div>

	<template v-if="number == 'hello'">
		<h4>HI</h4>
		<h4>Refat</h4>
		<h4>Whats Up</h4>
	</template>

</template>

<script>
export default {
	name: "App",
	data() {
		return {
			number: "hello",

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
			highlightColor: "orange",
			headerSize: 40,
			h2StyleObject: {
				color: "orange",
				fontSize: "40px",
				padding: "32px",
			},

			baseStyleObject: {
				fontSize: "43px",
				padding: "13px",
			},
			successStyleObject: {
				color: "white",
				backgroundColor: "green",
				border: "1px solid white",
			},
			dangerStyleObject: {
				color: "white",
				backgroundColor: "red",
				border: "2px solid white",
			},
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
