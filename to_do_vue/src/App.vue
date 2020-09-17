<template>
  <div id="app">
    <Todos v-bind:todos="todos" v-on:delete-todo="deleteTodo" />
    <AddTodo v-on:add-todo="addTodo" />
  </div>
</template>
<script>
import Todos from "./components/Todos";
import AddTodo from "./components/AddTodo";
export default {
  name: "app",
  components: {
    Todos,
    AddTodo
  },
  data() {
    return {
      todos: [
        {
          id: 1,
          title: "Code for 1 hour",
          completed: false
        },
        {
          id: 2,
          title: "Work on blog post",
          completed: false
        },
        {
          id: 3,
          title: "Duolingo practice",
          completed: false
        },
        {
          id: 4,
          title: "Cook Dinner",
          completed: false
        }
      ]
    };
  },
  methods: {
    addTodo(newTodoObj) {
      this.todos = [...this.todos, newTodoObj];
    },
    deleteTodo(todoId) {
      this.todos = this.todos.filter(todo => todo.id !== todoId);
    }
  }
};
</script>
<style>
#app {
  background-color: rgb(255, 255, 136);
  font-family: "Shadows Into Light", cursive;
  display: flex;
  align-items: center;
  justify-content: center;
  height: 600px;
  width: 550px;
  background: linear-gradient(top, rgba(0, 0, 0, 0.05), rgba(0, 0, 0, 0.25));
  background-color: #fffd75;
  box-shadow: 5px 5px 10px -2px rgba(124, 108, 108, 0.3);
  z-index: 1;
}
</style>