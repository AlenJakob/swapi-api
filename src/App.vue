<template>
  <div id="app">
    <EmployeesList/>
  </div>
</template>

<script>
import "material-icons/iconfont/material-icons.css";
import EmployeesList from "./components/EmployeesList";
import Card from "./components/Card";
export default {
  name: "App",
  components: {
    EmployeesList
  }
};
</script>

<style>
@import url("https://fonts.googleapis.com/css?family=Roboto&display=swap");
body {
  background: rgba(30, 42, 49, 1);
}
#app {
  font-family: "Roboto", sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #fff;
  margin-top: 60px;
}
</style>
