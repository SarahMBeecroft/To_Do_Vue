<template>
  <div>
    <h2>My to-dos:</h2>
    <ul>
      <li v-bind:key="todo.id" v-for="todo in todos">
        <Todo v-bind:todo="todo" v-on:delete-todo="$emit('delete-todo', todo.id)" />
      </li>
    </ul>
  </div>
</template>

<script>
import Todo from "./Todo";
export default {
  name: "Todos",
  components: {
    Todo
  },
  props: ["todos"]
};
</script>

<style scoped>
h2 {
  color: rgb(70, 70, 70);
  font-size: 2.5em;
  position: relative;
  left: 2.6em;
}
ul {
  list-style-type: none;
}
</style>


