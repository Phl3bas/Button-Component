<template>
  <div class="container">
    <div>
      <my-btn dark tile>Click Me</my-btn>
      <my-Btn yellow flat tall>Home</my-btn>
      <my-btn green round>About</my-btn>
      <my-btn red small>Sell Now</my-btn>
      <my-btn blue tall long>Buy Now</my-btn>
      <my-btn long>Contact</my-btn>
    </div>
  </div>
</template>

<script>
import myBtn from "./components/myBtn";

export default {
  name: "App",
  components: {
    myBtn
  }
};
</script>

<style>

div{
  display: grid;
  grid-template-columns: repeat(2, auto);
  grid-gap: 30px;
  width: 500px;
  justify-items: center;
}

my-btn{
  justify-self: center;
}

.container{
  position: absolute;
  top: 50vh;
  left: 50vw;
  transform: translate(-50%, -50%);
}


</style>
