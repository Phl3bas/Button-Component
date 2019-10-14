<template>
  <div class="container">
    <f-btn>Default</f-btn>
    <f-btn dark>dark</f-btn>
    <f-btn red>red</f-btn>
    <f-btn blue>blue</f-btn>
    <f-btn yellow>yellow</f-btn>
    <f-btn green>green</f-btn>
    <f-btn none>none</f-btn>

    <f-btn outline>outline</f-btn>
    <f-btn tall>tall</f-btn>
    <f-btn small>small</f-btn>
    <f-btn tile>tile</f-btn>
    <f-btn flat>flat</f-btn>
    <f-btn round>round</f-btn>
    <f-btn fill>fill</f-btn>
    <f-btn
      outline
      outlinecolor="#f0a314"
      textcolor="rgb(219, 120, 2)"
      bgcolor="#e6cb8c"
    >various color attr</f-btn>
    <f-btn long>long</f-btn>
  </div>
</template>

<script>
import fBtn from "./components/f-btn";

export default {
  name: "App",
  components: {
    fBtn: fBtn
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
