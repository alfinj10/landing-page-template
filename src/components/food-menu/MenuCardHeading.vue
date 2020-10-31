<template>
<div class="menu-card-heading-container">
      <h1 class="heading-text">Test</h1>
</div>
</template>

<script>

export default {

}
</script>

<style>

.menu-card-heading-container {
  display: flex;
  flex-direction: column;
  align-items: center;
  width: 400px;
  height: 60px;
  background: url(/assets/brush-stroke-red.png) no-repeat;
  background-size: contain;
  margin-bottom: 30px;
  margin-right: 50px;
  margin-left: 50px
}

.heading-text {
  font-family: 'Open Sans Condensed', sans-serif;
  color: #FCF200;
  text-transform: uppercase;
  letter-spacing: 5px;
  font-size: 32px;
  padding-top: 5px;
  display: flex;
  justify-content: center;
}

@media screen and (max-width:900px) {
  .menu-card-heading-container {
    width: 320px;
    height: 80px;
    margin: 0;
  }

  .heading-text{
      font-size: 26px;
      padding-top: 2px;
  }


}



/* @media screen and (max-width:600px) {
  .menu-card-heading-container {
    width: px;
    height: 75px;
  }

  .heading-text{
      font-size: 26px;
      padding-top: 2px;
  }


} */



</style>