<template>
  <div id="app">
    <eight-queen />
    <eight-queen-jsx />
  </div>
</template>

<script>
import EightQueen from "./components/EightQueen.vue";
import EightQueenJsx from "./components/EightQueenJsx.vue";
export default {
  name: "App",
  components: {
    EightQueen,
    EightQueenJsx,
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
