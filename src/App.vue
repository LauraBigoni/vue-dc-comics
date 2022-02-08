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
</style>
