<template>
  <footer>
    <div class="container">
      <div class="content">
        <section id="footer-nav">
          <ul>
            <h5>DC COMICS</h5>
            <li v-for="(comic, index) in comics" :key="index">
              <a :href="comic.url">{{ comic.text }}</a>
            </li>
            <h5>SHOP</h5>
            <li v-for="(shop, index) in shop" :key="index">
              <a :href="shop.url">{{ shop.text }}</a>
            </li>
          </ul>
          <ul>
            <h5>DC</h5>
            <li v-for="(dc, index) in dc" :key="index">
              <a :href="dc.url">{{ dc.text }}</a>
            </li>
          </ul>
          <ul>
            <h5>SITES</h5>
            <li v-for="(site, index) in sites" :key="index">
              <a :href="site.url">{{ site.text }}</a>
            </li>
          </ul>
        </section>
        <section class="bigger-logo">
          <img src="../assets/img/dc-logo-bg.png" alt="DC Logo" />
        </section>
      </div>
    </div>
    <section id="footer-social">
      <div class="container">
        <div class="sign-up">
          <a href="#">SIGN-UP NOW!</a>
        </div>
        <div class="socials">
          <h4>FOLLOW US</h4>
          <img src="../assets/img/footer-facebook.png" alt="Facebook" />
          <img src="../assets/img/footer-twitter.png" alt="Twitter" />
          <img src="../assets/img/footer-youtube.png" alt="YouTube" />
          <img src="../assets/img/footer-pinterest.png" alt="Pinterest" />
          <img src="../assets/img/footer-periscope.png" alt="Periscope" />
        </div>
      </div>
    </section>
  </footer>
</template>

<script>
export default {
  name: "Footer",
  data() {
    return {
      comics: [
        { text: "Characters", url: "#" },
        { text: "Comics", url: "#" },
        { text: "Movies", url: "#" },
        { text: "TV", url: "#" },
        { text: "Games", url: "#" },
        { text: "Videos", url: "#" },
        { text: "News", url: "#" },
      ],
      shop: [
        { text: "Shop DC", url: "#" },
        { text: "Shop DC Collectibles", url: "#" },
      ],
      dc: [
        { text: "Terms Of Use", url: "#" },
        { text: "Privacy policy (New)", url: "#" },
        { text: "Ad Choices", url: "#" },
        { text: "Advertising", url: "#" },
        { text: "Jobs", url: "#" },
        { text: "Subscriptions", url: "#" },
        { text: "Talent Workshops", url: "#" },
        { text: "CPSC Certificates", url: "#" },
        { text: "Ratings", url: "#" },
        { text: "Shop Help", url: "#" },
        { text: "Contact Us", url: "#" },
      ],
      sites: [
        { text: "DC", url: "#" },
        { text: "MAD Magazine", url: "#" },
        { text: "DC Kids", url: "#" },
        { text: "DC Universe", url: "#" },
        { text: "DC Power Visa", url: "#" },
      ],
    };
  },
};
</script>

<style scoped lang="scss">
$main_color: white;
$secondary_color: lightgrey;

footer {
  background-image: url("../assets/img/footer-bg.jpg");
  background-repeat: no-repeat;
  background-size: cover;
  display: flex;
  flex-direction: column;
  color: $main_color;

  .container {
    position: relative;

    .content {
      display: flex;
      flex-direction: row;
      justify-content: space-between;

      .bigger-logo {
        position: relative;
        bottom: 0;
        left: 200px;
        width: 360px;
      }
    }
  }
  a {
    color: $secondary_color;
  }

  #footer-nav {
    display: flex;

    h5 {
        padding: 20px 0;
        font-size: 20px;
    }
    ul {
      list-style-type: none;
      padding-right: 20px;

      li {
          line-height: 20px;
        font-size: 14px;
      }
    }
  }

  #footer-social {
    background-color: #303030;
    padding: 50px 0;

    .container {
      display: flex;
      align-items: center;
      justify-content: space-between;

      a {
        padding: 10px;
        border: 2px solid dodgerblue;
      }

      img {
        padding: 0 10px;
      }

      .sign-up {
        font-weight: bold;
      }

      .socials {
        display: flex;
        align-items: center;

        h4 {
          color: dodgerblue;
          padding-right: 10px;
          font-size: 20px;
        }
      }
    }
  }
}
</style>