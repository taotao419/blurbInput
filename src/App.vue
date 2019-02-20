<template>
  <div id="app">
    <img src="./assets/logo.png">
    <TodoList/>
  </div>
</template>

<script>
import TodoList from './components/TodoList.vue'
export default {
  components:{
    TodoList
  }
};
</script>

<style>
/* @import './variables.scss'; */

#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

h1 {
	text-align: center;
}
</style>
