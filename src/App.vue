<template>
  <div class="container">
    <div>
      <fbtn dark tile>Click Me</fbtn>
      <fbtn yellow flat tall>Home</fbtn>
      <fbtn green round>About</fbtn>
      <fbtn red small>Sell Now</fbtn>
      <fbtn blue tall long>Buy Now</fbtn>
      <fbtn>Contact</fbtn>
    </div>
  </div>
</template>

<script>
import fbtn from "./components/f-btn";

export default {
  name: "App",
  components: {
    fbtn
  }
};
</script>

<style>
div {
  display: grid;
  grid-template-columns: repeat(2, auto);
  grid-gap: 30px;
  width: 500px;
  justify-items: center;
}

my-btn {
  justify-self: center;
}

.container {
  position: absolute;
  top: 50vh;
  left: 50vw;
  transform: translate(-50%, -50%);
}
</style>
