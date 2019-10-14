<template>
  <div
    class="btn"
    :class="{
    red  : red,
    yellow : yellow, 
    blue : blue,
    dark : dark, 
    green : green,
    tall: tall,
    long: long,
    small: small,
    tile: tile,
    flat : flat,
    round : round,
    outline: outline,
    fill: fill,
    none: none,
    }"
    :style="{
      height: height,
      width: width,
      color: textcolor,
      }"
  >
    <span class="inner-text" :style="{fontSize: textsize}">
      <slot/>
    </span>
  </div>
</template>

<script>
export default {
  name: "fBtn",
  props: {
    red: Boolean,
    blue: Boolean,
    yellow: Boolean,
    green: Boolean,
    dark: Boolean,
    tall: Boolean,
    long: Boolean,
    small: Boolean,
    tile: Boolean,
    flat: Boolean,
    round: Boolean,
    outline: Boolean,
    none: Boolean,
    fill: Boolean,
    height: String,
    width: String,
    textsize: String,
    textcolor: String,
    outlinecolor: String,
    bgcolor: String
  },
  mounted() {
    this.outlinecolor ? (this.$el.style.borderColor = this.outlinecolor) : 0;
    this.bgcolor ? (this.$el.style.backgroundColor = this.bgcolor) : 0;
  }
};
</script>

<style scoped>
.btn {
  display: inline-block;
  position: relative;
  border-radius: 5px;
  height: 40px;
  width: 100px;
  padding: 0 010px;
  box-shadow: 0 2px 3px 1px rgba(0, 0, 0, 0.4);
  transition: all 200ms ease;
  margin: 5px;
  cursor: pointer;
  background-color: rgb(248, 248, 248);
  color: rgb(134, 134, 134);
  user-select: none;
  padding: 5px;
}

.btn:hover {
  box-shadow: 0 5px 6px 1px rgba(0, 0, 0, 0.3);
  transform: translatey(-1px);
}

.inner-text {
  display: inline-block;
  width: 100%;
  position: absolute;
  font-family: Arial, Helvetica, sans-serif;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  text-align: center;
  font-weight: bold;
}

.btn:active {
  box-shadow: 0 2px 1px 1px rgba(0, 0, 0, 0.3);
  transform: translatey(0);
}

.none {
  box-shadow: none;
  border: none;
  background-color: transparent;
  border-radius: 0;
  color: black;
}

.none:hover {
  box-shadow: none;
  transform: none;
}

.red {
  background-color: rgb(235, 77, 77);
  color: rgb(252, 209, 209);
  text-shadow: 1px 2px 3px rgb(153, 40, 40);
}

.blue {
  background-color: rgb(68, 70, 167);
  color: rgb(191, 187, 255);
  text-shadow: 1px 2px 3px rgb(27, 29, 100);
}

.yellow {
  background-color: rgb(244, 247, 112);
  color: rgb(116, 136, 4);
  text-shadow: 1px 1px 3px rgba(132, 136, 19, 0.5);
}

.green {
  background-color: rgb(90, 189, 95);
  color: rgb(210, 255, 205);
  text-shadow: 1px 2px 3px rgb(32, 112, 36);
}

.dark {
  background-color: rgb(68, 67, 67);
  color: white;
  text-shadow: 1px 2px 3px rgba(68, 67, 67, 0.5);
}

.small {
  height: 30px;
  width: 40px;
  font-size: 13px;
}

.long {
  width: 200px;
}

.tall {
  height: 60px;
}

.round {
  border-radius: 20px;
}

.tile {
  border-radius: 0;
}

.flat {
  box-shadow: none;
}

.outline {
  border: 2px solid rgba(0, 0, 0, 0.4);
  box-shadow: none;
  color: rgba(0, 0, 0, 0.6);
  font-weight: bold;
}

.fill {
  display: inline-block;
  height: 100%;
}

/*
TODO: add multiple outline-classes/props for different colors
TODO: add color, text-color and outline-color prop that takes HEX value for further customisation
TODO: add fill prop that defaults to 100% height
*/
</style>
