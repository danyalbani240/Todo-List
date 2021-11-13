<template>
  <div><addTodo @tValue="pushTodo" /> <todo-list :todoList="todoList" /></div>
</template>

<script>
import { ref } from "@vue/reactivity";
import addTodo from "./components/addForm.vue";
import TodoList from "./components/todoList.vue";
export default {
  name: "App",
  components: { addTodo, TodoList },
  setup() {
    const todoList = ref([]);
    const pushTodo = (value) => {
      todoList.value.push(value);
    };
    return { todoList, pushTodo };
  },
};
</script>

<style lang="scss">
* {
  margin: 0;
  padding: 0;
}
</style>
