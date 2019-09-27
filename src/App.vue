<template>
  <div class="container">
    <div>
      <fbtn dark flat tile height="70" width="220" textsize="1.5">Click Me</fbtn>
      <fbtn red long>Home</fbtn>
      <fbtn green tall>About</fbtn>
      <fbtn yellow round textsize="1.2">Sell Now</fbtn>
      <fbtn blue flat small>Buy Now</fbtn>
      <fbtn none outline textsize="1.2">Contact</fbtn>
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
