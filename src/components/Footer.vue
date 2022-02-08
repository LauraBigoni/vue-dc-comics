<template>
  <footer>
    <div class="container">
      <section id="footer-nav">
        <ul>
          <h5>titolo</h5>
          <li><a href="#">link</a></li>
          <li><a href="#">link</a></li>
          <li><a href="#">link</a></li>
          <li><a href="#">link</a></li>
          <li><a href="#">link</a></li>
        </ul>
      </section>
    </div>
    <section id="footer-social">
      <div class="container">
        <div class="sign-up">
          <a href="#">SIGN-UP NOW!</a>
        </div>
        <div class="socials">
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
};
</script>

<style scoped lang="scss">
$main_color: white;
$secondary_color: lightgrey;

footer {
  background-image: url("../assets/img/footer-bg.jpg");
  background-repeat: no-repeat;
  background-size: cover;
  padding-top: 200px;
  display: flex;
  flex-direction: column;
  color: $main_color;

  a {
    color: $secondary_color;
    text-decoration: none;
  }

  #footer-nav {
    ul {
      list-style-type: none;
      text-decoration: none;

      li {
        padding: 5px 0;
      }
    }
  }

  #footer-social {
    background-color: #303030;
    padding: 50px 0;
    margin-bottom: 20px;

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
    }
  }
}
</style>