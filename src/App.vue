<template>
  <div id="app">
    <Header />
  </div>
</template>

<script>
import Header from './components/Header.vue'

export default {
  name: 'App',
  components: {
    Header,
  }
}
</script>

<style lang="scss">
$main_font: 'Segoe UI', 'Open Sans', Helvetica, sans-serif;
$lighter_font: 'Segoe UI Light', 'Open Sans', Helvetica, sans-serif;

#app {
  font-family: $main_font;
}

* {
  margin:0;
  padding: 0;
  box-sizing: border-box;
}

.container {
  max-width: 1200px;
  margin: 0 auto;
}
</style>
