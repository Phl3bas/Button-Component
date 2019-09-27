<template>
  <div class="container">
    <div>
      <fbtn>Default</fbtn>
      <fbtn dark>dark</fbtn>
      <fbtn red>red</fbtn>
      <fbtn blue>blue</fbtn>
      <fbtn yellow>yellow</fbtn>
      <fbtn green>green</fbtn>
      <fbtn none>none</fbtn>

      <fbtn outline>outline</fbtn>
      <fbtn tall>tall</fbtn>
      <fbtn small>small</fbtn>
      <fbtn tile>tile</fbtn>
      <fbtn flat>flat</fbtn>
      <fbtn long>long</fbtn>
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
.container {
  position: absolute;
  top: 50vh;
  left: 50vw;
  transform: translate(-50%, -50%);
}

div {
  display: grid;
  grid-template-columns: repeat(3, 200px);
  justify-items: center;
  align-items: center;
  grid-gap: 10px;
}

div:last-child {
  grid-column: 1 / 4;
}
</style>
