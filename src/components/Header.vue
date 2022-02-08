<template>
  <div>
    <header>
      <div class="container">
        <div class="logo">
          <img src="../assets/img/dc-logo.png" alt="DC Logo" />
        </div>
        <nav class="nav-menu">
          <ul>
            <li v-for="(nav, index) in navbar" :key="index"><a :href="nav.url">{{nav.text}}</a></li>
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
        { text: "CHARACTERS", url: "#" },
        { text: "COMICS", url: "#" },
        { text: "MOVIES", url: "#" },
        { text: "TV", url: "#" },
        { text: "GAMES", url: "#" },
        { text: "COLLECTIBLES", url: "#" },
        { text: "VIDEOS", url: "#" },
        { text: "FANS", url: "#" },
        { text: "NEWS", url: "#" },
        { text: "SHOP", url: "#" },
      ]
    }
  }
};
</script>

<style scoped lang="scss">
header {
  background-color: white;
  padding: 10px 0;
  margin-top: 20px;

  .container {
    display: flex;
    align-items: center;
    justify-content: space-between;

    ul {
      display: flex;
      list-style-type: none;

      li {
        padding: 10px;

        a {
          color: #303030;
          font-weight: bold;
        }
      }
    }
  }
}
</style>
