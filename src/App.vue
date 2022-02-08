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
$main_font: "Segoe UI", "Open Sans", Helvetica, sans-serif;
$lighter_font: "Segoe UI Light", "Open Sans", Helvetica, sans-serif;

#app {
  font-family: $main_font;
}

* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

.container {
  max-width: 1200px;
  margin: 0 auto;
}

img {
  max-width: 100%;
  height: auto;
}

body {
  height: calc(100vh - 40px);
  background-color: black;
}

#secondary-nav,
footer li {
  font-family: $lighter_font;
}
</style>
