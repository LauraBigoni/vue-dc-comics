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
        { text: "COMICS", url: "#", active: false },
        { text: "MOVIES", url: "#", active: true },
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
      li.active {
        background-color: lightblue;
      }
    }
  }
}
</style>
