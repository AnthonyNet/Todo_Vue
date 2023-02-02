<script setup>
import TodoCreator from '../components/TodoCreator.vue';
import {uid} from "uid";
const todoList =ref([]);

const createTodo = (todo) => {
  todoList.value.push({
    id: uid(),
    todo,
    isCompleted: false,
    isEditing: null,
  });
}
</script>

<template>
  <main>
    <TodoCreator @create-todo="createTodo"/>
  </main>
</template> 

<style lang="scss">
</style>