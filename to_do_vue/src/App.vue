<template>
  <div id="app">
    <Todos />
  </div>
</template>

<script>
import Todos from "../src/components/Todos";
export default {
  name: "app",
  components: {
    Todos
  },
  data() {
    return {
      todos: [
        {
          id: 1,
          title: "Go for a walk",
          completed: false
        },
        {
          id: 2,
          title: "One hour of coding",
          completed: false
        },
        {
          id: 3,
          title: "Make dinner",
          completed: false
        },
        {
          id: 4,
          title: "Do Laundry",
          completed: false
        },
        {
          i: 5,
          title: "Finish monthly report",
          completed: false
        }
      ]
    };
  }
};
</script>

<style>
</style>
