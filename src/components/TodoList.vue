<template>
  <div>
    <ul>
      {{todos}}
      <TodoItem
      v-for="todo of todos"
      v-bind:todo="todo"
      />
    </ul>
  </div>
</template>

<script>
// экспорт TodoItem из TodoItem.vue
import TodoItem from "@/components/TodoItem";
export default {
  // props -properties, 'todos' - элемент, который мы принимаем из App
  props: ['todos'],
  components: {
    TodoItem: TodoItem
  }
}
</script>

<style scoped>

</style>