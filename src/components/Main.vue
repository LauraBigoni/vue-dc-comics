<template>
	<main>
		<section id="jumbotron"></section>
		<section id="comics">
			<div class="container">
				<div class="currentSeries">
					<p>CURRENT SERIES</p>
				</div>
				<Comics />
				<div class="load-more">
					<p>LOAD MORE</p>
				</div>
			</div>
		</section>
		<section id="secondary-nav">
			<div class="container">
				<Products :products="products" />
			</div>
		</section>
	</main>
</template>

<script>
import Comics from "./Comics.vue";
import Products from "./Products.vue";

export default {
	name: "Main",
	components: {
		Comics,
		Products,
	},
	props: ["products"],
};
</script>

<style scoped lang="scss">
@import "../assets/scss/_vars.scss";

main {
	color: white;
	background-color: #1c1c1c;

	.container {
		position: relative;
		padding: 50px 0;
		display: flex;
		flex-wrap: wrap;
		justify-content: center;
	}

	#jumbotron {
		background-image: url("../assets/img/jumbotron.jpg");
		background-repeat: no-repeat;
		background-position: top center;
		background-size: cover;
		height: 400px;
	}

	.currentSeries {
		width: fit-content;
		padding: 10px;
		font-weight: bold;
		background-color: dodgerblue;
		position: absolute;
		top: -20px;
		left: 0;
		cursor: pointer;
	}

	.load-more {
		width: 200px;
		text-align: center;
		padding: 10px;
		font-weight: bold;
		background-color: dodgerblue;
		cursor: pointer;
	}
	#secondary-nav {
		background-color: dodgerblue;
	}
}
</style>