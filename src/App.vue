<template>
  <div :class="theme === 'light' ? 'light-theme' : 'dark-theme'" id="app" class="container">
    <button @click="changeTheme">switch theme</button>
    <todo-list></todo-list>
  </div>
</template>

<script>
import TodoList from './components/TodoList.vue'

export default {
  name: 'App',
  components: {
    TodoList,
  },
  data () {
    return {
      theme: "light"
    }
  }, 
  methods: {
    changeTheme() {
      console.log("am changing theme");
      this.theme = this.theme === "dark" ? "light" : "dark";
    }
  }
}
</script>

<style>

* {
  box-sizing: border-box;
}

.container {
  max-width: 600px;
  margin: 0 auto;
}


#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  /* text-align: center; */
  color: #2c3e50;
  margin-top: 60px;
  font-size: 24px;
  align-items: center;
}
.light-theme {
  background-color: white;
  color: black;
}
.dark-theme {
  background-color: black;
  color: white;
}
</style>