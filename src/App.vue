<template>
  <div id="app">
    <todo-app></todo-app>
  </div>
</template>

<script>
import TodoApp from './components/TodoApp.vue'

export default {
  name: 'App',
  components: {
    TodoApp
  }
}
</script>

<style scoped>

body {
  font-family: 'Poppins', sans-serif;
  background-color: rgb(29, 29, 31);
}
.app {
  height: 100%;
  margin: 0;
  padding: 0;
}
</style>
