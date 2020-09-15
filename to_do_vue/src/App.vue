<template>
  <div id="app">
    <Test />
  </div>
</template>

<script>
import Test from "./components/Test.vue";

export default {
  name: "App",
  components: {
    Test
  }
};
</script>

<style>
body {
  background-color: black;
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  margin-top: 60px;
}
</style>
