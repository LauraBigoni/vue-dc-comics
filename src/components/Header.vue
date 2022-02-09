<template>
	<div>
		<header>
			<div class="container">
				<div class="logo">
					<img src="../assets/img/dc-logo.png" alt="DC Logo" />
				</div>
				<nav class="nav-menu">
					<ul>
						<li
							v-for="(nav, index) in navbar"
							:key="index"
							:class="{ active: nav.active }"
						>
							<a :href="nav.url">{{ nav.text }}</a>
						</li>
					</ul>
				</nav>
			</div>
		</header>
	</div>
</template>

<script>
export default {
	name: "Header",
	data() {
		return {
			navbar: [
				{ text: "CHARACTERS", url: "#", active: false },
				{ text: "COMICS", url: "#", active: true },
				{ text: "MOVIES", url: "#", active: false },
				{ text: "TV", url: "#", active: false },
				{ text: "GAMES", url: "#", active: false },
				{ text: "COLLECTIBLES", url: "#", active: false },
				{ text: "VIDEOS", url: "#", active: false },
				{ text: "FANS", url: "#", active: false },
				{ text: "NEWS", url: "#", active: false },
				{ text: "SHOP", url: "#", active: false },
			],
		};
	},
};
</script>

<style scoped lang="scss">
header {
	background-color: white;

	.container {
		display: flex;
		align-items: center;
		justify-content: space-between;

		.logo img {
			width: 80px;
			height: auto;
		}
		.nav-menu {
			display: flex;
		}
		ul {
			display: flex;
			list-style-type: none;
			align-items: center;

			li {
				padding: 60px 0;
				margin-right: 15px;
				border-bottom: 4px solid transparent;

				a {
					color: #303030;
					font-weight: bold;
				}
			}

			li.active {
				border-bottom: 4px solid dodgerblue;
			}

			li:hover {
				border-bottom: 4px solid dodgerblue;
			}
		}
	}
}
</style>
