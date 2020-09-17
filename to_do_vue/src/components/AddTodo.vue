<template>
  <div>
    <form @submit="addTodo">
      <input type="text" v-model="title" name="title" />
      <button type="submit">Add</button>
    </form>
  </div>
</template>
<script>
import uuid from "uuid";
export default {
  name: "AddTodo",
  data() {
    return {
      title: ""
    };
  },
  methods: {
    addTodo(e) {
      e.preventDefault();
      const newTodoObj = {
        id: uuid.v4(),
        title: this.title,
        completed: false
      };
      this.$emit("add-todo", newTodoObj);
      this.title = "";
    }
  }
};
</script>
<style scoped>
button {
  background-color: rgb(255, 255, 136);
  margin: 6px;
  font-family: "Shadows Into Light", cursive;
  height: 30px;
  position: relative;
  top: 200px;
  right: 110px;
}
input {
  height: 24px;
  position: relative;
  top: 200px;
  right: 112px;
}
</style>