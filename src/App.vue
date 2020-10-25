<template>
  <div id="app">
    <Navbar />
  </div>
</template>

<script>
import Navbar from './components/Navbar.vue'

export default {
  name: 'App',
  components: {
    Navbar
  }
}
</script>

<style>

* {
  margin: 0;
  padding: 0px;
  box-sizing: border-box;
}

</style>
