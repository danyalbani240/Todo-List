<template>
  <form @submit.prevent="sendTodo">
    <input v-model="todo" type="text" />
    <button>Add</button>
  </form>
</template>

<script>
import { ref } from "vue";
export default {
  setup(props, context) {
    const todo = ref("");
    const sendTodo = () => {
      if (todo.value != "") context.emit("tValue", todo.value);
      todo.value = "";
    };
    return { todo, sendTodo };
  },
};
</script>

<style lang="scss" scoped>
input {
  width: 200px;
  padding: 10px 0;
}
button {
  padding: 10px 10px;
}
</style>
