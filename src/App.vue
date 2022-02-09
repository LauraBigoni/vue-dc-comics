<template>
	<div id="app">
		<Header />
		<Main :products="products"/>
		<Footer />
	</div>
</template>

<script>
import Header from "./components/Header.vue";
import Main from "./components/Main.vue";
import Footer from "./components/Footer.vue";

export default {
	name: "App",
	components: {
		Header,
		Main,
		Footer,
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

<style lang="scss">
@import "./assets/scss/style.scss";

#app {
	font-family: $main_font;
}

#secondary-nav,
footer li {
	font-family: $lighter_font;
}
</style>
