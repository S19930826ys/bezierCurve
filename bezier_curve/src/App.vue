<template>
  <div id="app">
    <bezierCurve></bezierCurve>
  </div>
</template>

<script>
import bezierCurve from "./components/bezierCurve.vue";

export default {
  name: "App",
  components: {
    bezierCurve,
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
  margin-top: 30px;
}
</style>
