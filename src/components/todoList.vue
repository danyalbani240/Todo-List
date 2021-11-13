<template>
  <div>
    <div v-for="todo in todoList" :key="todo">
      {{ todo }}
    </div>
  </div>
</template>

<script>
export default {
  props: {
    todoList: {
      type: Array,
      required: true,
    },
  },
};
</script>

<style></style>
