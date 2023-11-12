<template>
  <div class="todo-list">
    <ToDoItem
    v-for="todo in todos"
      :key="todo.id"
      :title="todo['title']"
      :description="todo['description']"
    />
  </div>
</template>

<script>

import ToDoItem from '@/components/TodoItem';

export default {
  components: {
    ToDoItem
  },
  props: {
    todos: {
      required: true,
      type: Array
    }
  }
}

</script>

<style lang="scss" scoped>
.todo {

  &-container {
    /* margin: 0 auto; */
    width: 400px;
    min-height: 400px;
    background-color: #ededed;
  }
}
</style>