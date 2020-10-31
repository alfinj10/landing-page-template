<template>
  <div class="menu-section">
      <div class="menu-card">
            <MenuCardHeading />
            <MenuCardHeading />
            <MenuCardHeading />
            <MenuCardHeading />
            <MenuCardHeading />
      </div>
  </div>
</template>

<script>
import MenuCardHeading from './MenuCardHeading.vue'
export default {

    name: 'MenuSection',
    components: {
        MenuCardHeading
    }

}
</script>

<style>

.menu-section {
    padding-top: 20px;
    display: flex;
    justify-content: center;
    background-color: lightgrey;

}

.menu-card {
    display: flex;
    flex-wrap: wrap;
    flex-direction: row;
    justify-content: space-evenly;
    /* flex-basis: 85% */
}


</style>