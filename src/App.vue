<template>
  <div id="app">

    <Navbar />
    <Menusection />
  </div>
</template>

<script>
import Navbar from './components/Navbar.vue'
import Menusection from './components/food-menu/Menusection.vue'

export default {
  name: 'App',
  components: {
    Navbar,
    Menusection
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
