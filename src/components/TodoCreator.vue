<script setup>
import {ref, defineEmits} from "vue";

const emit = defineEmits(["createTodo"])

const todo = ref('');



const createTodo = () => {
    emit('create-todo', todo.value);
}

</script>

<template lang="">
    <div class="input-wrap">
        <input type="text" v-model="todo.todo" />
        <button @click="createTodo()">Create</button>
    </div>
    <p>{{ todo.todo }}</p>
</template>

<style lang="scss" scoped>
.input-wrap {
    display: flex;
    transition: 250ms ease;
    border: 2px solid #41b080;
    &.input-err {
      border-color: red;
    }
    &:focus-within {
      box-shadow: 0 -4px 6px -1px rgb(0 0 0 / 0.1),
        0 -2px 4px -2px rgb(0 0 0 / 0.1);
    }
    input {
      width: 100%;
      padding: 8px 6px;
      border: none;
      &:focus {
        outline: none;
      }
    }
    button {
      padding: 8px 16px;
      border: none;
    }
  }
  p{
    color: red;
  }
  .err-msg {
    margin-top: 6px;
    font-size: 12px;
    text-align: center;
    color: red;
  }
</style>