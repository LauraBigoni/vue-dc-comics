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
				<ul>
					<li v-for="(product, index) in products" :key="index">
						<img
							:class="{ resized: product.resized }"
							:src="require('../assets/img/' + product.img)"
						/>
						<a :href="product.url">{{ product.text }}</a>
					</li>
				</ul>
			</div>
		</section>
	</main>
</template>

<script>
import Comics from "./Comics.vue";

export default {
	name: "Main",
	components: {
		Comics,
	},
	data() {
		return {
			products: [
				{
					img: "buy-comics-digital-comics.png",
					text: "DIGITAL COMICS",
					url: "#",
					resized: true,
				},
				{
					img: "buy-comics-merchandise.png",
					text: "DC MERCHANDISE",
					url: "#",
					resized: false,
				},
				{
					img: "buy-comics-subscriptions.png",
					text: "SUBSCRIPTION",
					url: "#",
					resized: false,
				},
				{
					img: "buy-comics-shop-locator.png",
					text: "COMIC SHOP LOCATOR",
					url: "#",
					resized: true,
				},
				{
					img: "buy-dc-power-visa.svg",
					text: "DC POWER VISA",
					url: "#",
					resized: false,
				},
			],
		};
	},
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
}

#secondary-nav {
	background-color: dodgerblue;

	ul {
		list-style-type: none;
		display: flex;
		justify-content: space-around;

		li {
			padding: 10px;
			display: flex;
			align-items: center;

			img {
				width: 50px;
				height: 56px;
				margin-right: 10px;
				color: $secondary_color;
			}

			img.resized {
				width: 40px;
			}

			a {
				color: $secondary_color;
				font-weight: bolder;
			}
		}
	}
}
</style>