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
          <li><a href="#">prodotto1</a></li>
          <li><a href="#">prodotto2</a></li>
          <li><a href="#">prodotto3</a></li>
          <li><a href="#">prodotto4</a></li>
          <li><a href="#">prodotto5</a></li>
          <li><a href="#">prodotto6</a></li>
          <li><a href="#">prodotto7</a></li>
        </ul>
      </div>
    </section>
  </main>
</template>

<script>
export default {
  name: "Main",
};
</script>

<style scoped lang="scss">
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
      }
    }
  }
}
</style>