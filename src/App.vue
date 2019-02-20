<template>
  <div id="app">
    <img src="./assets/logo.png">
    <router-view/>
    <el-checkbox v-model="checked">Check Or Not</el-checkbox>
  </div>
</template>

<script>
export default {
  name: "App",
  data() {
    return {
      checked: true
    };
  }
};
</script>

<style>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
