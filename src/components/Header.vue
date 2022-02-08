<template>
  <div>
    <header>
      <div class="container">
        <div class="logo">
          <img src="../assets/img/dc-logo.png" alt="DC Logo" />
        </div>
        <nav class="nav-menu">
          <ul>
            <li><a href="#">link1</a></li>
            <li><a href="#">link2</a></li>
            <li><a href="#">link3</a></li>
            <li><a href="#">link4</a></li>
            <li><a href="#">link5</a></li>
            <li><a href="#">link6</a></li>
            <li><a href="#">link7</a></li>
            <li><a href="#">link8</a></li>
            <li><a href="#">link9</a></li>
            <li><a href="#">link10</a></li>
          </ul>
        </nav>
      </div>
    </header>
  </div>
</template>

<script>
export default {
  name: "Header",
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
          text-decoration: none;
        }
      }
    }
  }
}
</style>
