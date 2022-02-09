<template>
	<ul>
		<li v-for="(product, index) in products" :key="index">
			<img
				:class="{ resized: product.resized }"
				:src="require('../assets/img/' + product.img)"
			/>
			<a :href="product.url">{{ product.text }}</a>
		</li>
	</ul>
</template>

<script>
export default {
	name: "Products",
	props: ["products"],
};
</script>

<style scoped lang="scss">
@import "../assets/scss/_vars.scss";
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
</style>