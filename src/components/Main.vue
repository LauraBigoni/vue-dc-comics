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
          <li v-for="(product, index) in products" :key="index"><a :href="product.url">{{product.text}}</a></li>
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
        { img: '../assets/img/buy-digital-comics.png' , text: "DIGITAL COMICS", url: "#" },
        { img: '../assets/img/buy-comics-merchandise.png' , text: "DC MERCHANDISE", url: "#" },
        { img: '../assets/img/buy-comics-subscriptions.png' , text: "SUBSCRIPTION", url: "#" },
        { img: '../assets/img/buy-comics-shop-locator.png' , text: "COMIC SHOP LOCATOR", url: "#" },
        { img: '../assets/img/buy-dc-power-visa.svg' , text: "DC POWER VISA", url: "#" },
      ]
    }
  }
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
    padding: 50px 0;
  }

  #secondary-nav {
    background-color: dodgerblue;
    padding: 50px 0;

    ul {
      list-style-type: none;
      display: flex;
      justify-content: space-around;

      li {
        padding: 10px;

        a {
          color: $secondary_color;
          font-weight: bolder;
        }
      }
    }
  }
}
</style>