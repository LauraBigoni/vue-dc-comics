<template>
  <main>
    <div class="container">
      <section id="comics">
        <h1>Contenuto della pagina qui</h1>
      </section>
    </div>
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
    };
  },
};
</script>

<style scoped lang="scss">
$secondary_color: lightgrey;

main {
  color: white;

  #comics {
    display: flex;
    align-items: center;

    // TODO: Rimuovere
    padding: 35px 0;
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