<template>
  <div class="container">
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
    <fbtn round>round</fbtn>
    <fbtn fill>fill</fbtn>
    <fbtn
      outline
      outlinecolor="#f0a314"
      textcolor="rgb(219, 120, 2)"
      bgcolor="#e6cb8c"
    >various color attr</fbtn>
    <fbtn long>long</fbtn>
  </div>
</template>

<script>
import fbtn from "./components/f-btn";

export default {
  name: "App",
  components: {
    fbtn
  },
  data: () => {
    return {
      clickHandler: false
    };
  }
};
</script>

<style>
body {
  overflow: hidden;
}
.container {
  position: absolute;
  top: 50vh;
  left: 50%;
  transform: translate(-50%, -50%);
}

div {
  display: grid;
  grid-template-columns: repeat(3, 200px);
  grid-template-rows: 100px 100px 100px 100px 100px 100px;
  justify-items: center;
  align-items: center;
}

div:last-child {
  grid-column: 1 / 4;
}
</style>
