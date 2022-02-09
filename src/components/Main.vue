<template>
	<main>
		<section id="jumbotron"></section>
		<section id="comics">
			<div class="container">
				<div class="currentSeries">
					<p>CURRENT SERIES</p>
				</div>
				<ul>
					<li v-for="(comic, index) in comics" :key="index">
						<div class="card"><img :src="comic.thumb" :alt="comic.type" /></div>
						<p class="comic-series">{{ comic.series }}</p>
					</li>
				</ul>
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
export default {
	name: "Main",
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
			comics: [
				{
					thumb:
						"https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2018/09/AC1000_DLX_162-001_HD_5ba13723281ab0.37845353.jpg?itok=ZsI-C5eX",
					price: "$19.99",
					series: "Action Comics",
					type: "comic book",
				},
				{
					thumb:
						"https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2020/09/AV1976_01_300-001_HD_5f738f6e39ddd7.18205602.jpg?itok=VgdYdJ01",
					price: "$3.99",
					series: "American Vampire 1976",
					type: "comic book",
				},
				{
					thumb:
						"https://www.dccomics.com/sites/default/files/styles/covers192x291/public/gn-covers/2018/08/AQMv4_UW_153-001_HD_5b7efa1745a9b8.08589135.jpg?itok=HPTtnrsb",
					price: "$16.99",
					series: "Aquaman",
					type: "graphic novel",
				},
				{
					thumb:
						"https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2018/06/batgirl_v5_1_5b23e1f1124941.50950783.jpg?itok=VnrJah76",
					price: "$2.99",
					series: "Batgirl",
					type: "comic book",
				},
				{
					thumb:
						"https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2018/09/BM_56_300-001_HD_5ba137a85c3bf3.33122291.jpg?itok=3FHJQYJZ",
					price: "$3.99",
					series: "Batman",
					type: "comic book",
				},
				{
					thumb:
						"https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2018/09/BM_56_300-001_HD_5ba137a85c3bf3.33122291.jpg?itok=3FHJQYJZ",
					price: "$2.99",
					series: "Batman Beyond",
					type: "comic book",
				},
				{
					thumb:
						"https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2019/08/BMSM_5d4361b7116261.74371456.jpg?itok=kEDR2OL8",
					price: "$3.99",
					series: "Batman/Superman",
					type: "comic book",
				},
				{
					thumb:
						"https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2020/09/BMSMANN_01_300-001_HD_5f5ff17fa1d665.74704970.jpg?itok=azz5sfGk",
					price: "$4.99",
					series: "Batman/Superman Annual",
					type: "comic book",
				},
				{
					thumb:
						"https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2020/09/BMTJWZ_01_300-001_HD_5f5ff2307dcb37.34652945.jpg?itok=VswVjLR8",
					price: "$5.99",
					series: "Batman: The Joker War Zone",
					type: "comic book",
				},
				{
					thumb:
						"https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2020/08/cover-v2_5f40314645a734.37285065.png?itok=ImNM2QBY",
					price: "$6.99",
					series: "Batman: Three Jokers",
					type: "comic book",
				},
				{
					thumb:
						"https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2020/10/BMWK_HQ_01_300-001_HD_5f7cb4945e13f6.89501032.jpg?itok=sVwALbUX",
					price: "$4.99",
					series: "Batman: White Knight Presents: Harley Quinn",
					type: "comic book",
				},
				{
					thumb:
						"https://www.dccomics.com/sites/default/files/styles/covers192x291/public/gn-covers/2019/04/CTWv1_CC_144-001_HD_5ca5299a751963.53054221.jpg?itok=ooPaoLDq",
					price: "$16.99",
					series: "Catwoman",
					type: "graphic novel",
				},
			],
		};
	},
};
</script>

<style scoped lang="scss">
$secondary_color: lightgrey;

main {
	color: white;
	background-color: #1C1C1C;

	#jumbotron {
		background-image: url("../assets/img/jumbotron.jpg");
		background-repeat: no-repeat;
		background-position: top center;
		background-size: cover;
		height: 400px;
	}

	#comics {
		.container {
			position: relative;
			padding: 50px 0;
			display: flex;
			flex-wrap: wrap;
			justify-content: center;
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

		ul {
			list-style-type: none;
			display: flex;
			flex-wrap: wrap;
			justify-content: space-around;

			li {
				margin: 20px 5px;
        width: 200px;
			}

			.card {
				width: 200px;
				height: 200px;
				overflow: hidden;
			}

      p {
        padding: 20px 0;
      }
			.comic-series {
				text-transform: uppercase;
			}
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
		padding: 30px 0;

		ul {
			list-style-type: none;
			display: flex;
			justify-content: space-around;

			li {
				padding: 10px;
				display: flex;
				align-items: center;

				img {
					width: 60px;
					height: 66px;
					margin-right: 10px;
          color: $secondary_color;
				}

				img.resized {
					width: 50px;
				}

				a {
					color: $secondary_color;
					font-weight: bolder;
				}
			}
		}
	}
}
</style>