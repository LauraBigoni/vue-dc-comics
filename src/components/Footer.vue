<template>
  <footer>
    <div class="container">
      <div class="content">
        <section id="footer-nav">
          <ul>
            <h5>DC COMICS</h5>
            <li v-for="(comic, i) in comics" :key="i">
              <a :href="comic.url">{{ comic.text }}</a>
            </li>
            <h5>SHOP</h5>
            <li v-for="(shop, i) in shop" :key="'A'+i">
              <a :href="shop.url">{{ shop.text }}</a>
            </li>
          </ul>
          <ul>
            <h5>DC</h5>
            <li v-for="(dc, i) in dc" :key="i">
              <a :href="dc.url">{{ dc.text }}</a>
            </li>
          </ul>
          <ul>
            <h5>SITES</h5>
            <li v-for="(site, i) in sites" :key="i">
              <a :href="site.url">{{ site.text }}</a>
            </li>
          </ul>
        </section>
        <section class="bigger-logo"></section>
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
@import "../assets/scss/_vars.scss";

footer {
  background-image: url("../assets/img/footer-bg.jpg");
  background-repeat: no-repeat;
  background-size: cover;
  display: flex;
  flex-direction: column;
  color: $main_color;

  .container {
    .content {
      display: flex;

      .bigger-logo {
        background-image: url("../assets/img/dc-logo-bg.png");
        background-repeat: no-repeat;
        background-position: right center;
        width: 700px;
      }
    }
  }

  a {
    color: $secondary_color;
  }

  #footer-nav {
    display: flex;
    margin: 40px;

    h5 {
      padding: 20px 0;
      font-size: 20px;
    }
    ul {
      list-style-type: none;
      padding-right: 30px;

      li {
        line-height: 20px;
        font-size: 14px;
      }
    }
  }

  #footer-social {
    background-color: #303030;
    padding: 40px 0;

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
        cursor: pointer;
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
          cursor: pointer;
        }
      }
    }
  }
}
</style>