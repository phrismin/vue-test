<template>
  <div id="app">
    <h1>Todo application</h1>
    <br>
    <TodoList
      v-bind:todos="todos"
    />
  </div>
</template>

<script>

// экспорт объектов из components
import TodoList from "@/components/TodoList";
export default {
  name: 'App',
  data() {
    return {
      todos: [
        {id: 1, title: 'Купить хлеб', completed: false},
        {id: 2, title: 'Купить хлеб', completed: false},
        {id: 3, title: 'Купить хлеб', completed: false}
      ]
    }
  },
  components: {
    TodoList: TodoList
  }
}
</script>

<!--стили для страницы-->
<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
