<template>
  <div v-bind:class="{ 'completed': todo.completed }" id="notes">
    <i class="fas fa-trash-alt" @click="$emit('delete-todo', todo.id)"></i>
    <p v-on:click="markComplete">{{ todo.title }}</p>
  </div>
</template>

<script>
export default {
  name: "Todo",
  props: ["todo"],
  methods: {
    markComplete() {
      this.todo.completed = !this.todo.completed;
    }
  }
};
</script>

<style scoped>
.completed {
  text-decoration: line-through;
}
#notes {
  position: relative;
  left: 76px;
  bottom: 65px;
}
p {
  color: rgb(70, 70, 70);
  font-size: 1.4em;
  margin: 2px;
}
.fa-trash-alt {
  position: relative;
  top: 33px;
  right: 25px;
  color: rgb(70, 70, 70);
}
</style>