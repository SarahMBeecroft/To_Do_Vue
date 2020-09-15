<template>
  <div>
    <h1>Hi, my name is Sarah</h1>
  </div>
</template>

<script>
export default {
  name: "Test",
  props: {
    msg: String
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
* {
  background-color: black;
}
h1 {
  font-family: Arial, Helvetica, sans-serif;
  font-size: 9em;
  color: rgb(140, 40, 227);
  text-align: center;
}
</style>
