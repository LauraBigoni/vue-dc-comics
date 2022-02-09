<template>
	<div id="app">
		<Header />
		<Main />
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
