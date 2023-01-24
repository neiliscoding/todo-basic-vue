<template>
  <div id="app">
    <ToDoList :state="state"></ToDoList>

  </div>
</template>

<script>
import ToDoList from "./components/ToDoList.vue";

export default {
  name: "App",
  components: {
    ToDoList,
  },
  data() {
    return {
      state: {
        showDone: true,
        todos : [
          {
            text: "Create mockups in figma",
            done: true,
          },          {
            text: "Create HTML prototype",
            done: false,
          },          {
            text: "Discuss reusable component strategy with PO",
            done: false,
          }
        ]
      }
    }
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}
@import './assets/bootstrap/css/bootstrap.min.css';
</style>
