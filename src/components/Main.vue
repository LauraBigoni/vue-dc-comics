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
          <li>prodotto1</li>
          <li>prodotto2</li>
          <li>prodotto3</li>
          <li>prodotto4</li>
          <li>prodotto5</li>
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
    height: 100px;
  }

  #secondary-nav {
    background-color: dodgerblue;
    padding: 40px 0;

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