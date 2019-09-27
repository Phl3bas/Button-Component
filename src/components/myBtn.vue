<template>
  <div
    class="btn"
    :class="{
    red  : red,
    yellow : yellow, 
    blue : blue,
    dark : dark, 
    green : green,
    large: large,
    medium: medium,
    small: small,
    tile: tile,
    flat : flat,
    round : round,
    outline: outline
    }"
  >
    <span class="inner-text">
      <slot/>
    </span>
  </div>
</template>

<script>
export default {
  name: "myBtn",
  props: {
    red: Boolean,
    blue: Boolean,
    yellow: Boolean,
    green: Boolean,
    dark: Boolean,
    large: Boolean,
    medium: Boolean,
    small: Boolean,
    tile: Boolean,
    flat: Boolean,
    round: Boolean,
    outline: Boolean
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
  box-shadow: 0 1px 3px rgba(0, 0, 0, 0.4);
  transition: all 200ms ease;
  margin: 5px;
}

.btn:hover {
  box-shadow: 0 3px 3px rgba(0, 0, 0, 0.4);
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
}

.btn:active {
  box-shadow: 0 1px 4px rgba(0, 0, 0, 0.4);
  color: black;
  transform: translatey(0);
}

.red {
  background-color: rgb(235, 77, 77);
  color: white;
  text-shadow: 1px 2px 3px rgba(0, 0, 0, 0.3);
}

.blue {
  background-color: rgb(68, 70, 167);
  color: rgb(255, 255, 255);
  text-shadow: 1px 2px 3px rgba(0, 0, 0, 0.3);
}

.yellow {
  background-color: rgb(244, 247, 112);
  color: rgb(60, 61, 54);
  text-shadow: 1px 2px 3px rgba(0, 0, 0, 0.3);
}

.green {
  background-color: rgb(90, 189, 95);
  color: white;
  text-shadow: 1px 2px 3px rgba(0, 0, 0, 0.3);
}

.dark {
  background-color: rgb(68, 67, 67);
  color: white;
  text-shadow: 1px 2px 3px rgba(255, 255, 255, 0.3);
}

.small {
  height: 35px;
  width: 60px;
  font-size: 13px;
}

.medium {
  height: 40px;
  width: 150px;
}

.large {
  height: 60px;
  width: 200px;
  font-size: 25px;
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
  border: 2px solid black;
  box-shadow: none;
}
</style>
