<template>
  <div id="app">
    <div class="container-fluid">
      <h1 class="mt-4 mb-4">Todo List</h1>
      <ul class="list-group" style="border-radius: 1em">
        <li class="list-group-item">
          <div class="form-check">
            <input
              class="form-check-input"
              type="checkbox"
              id="formCheck-1"
            /><label class="form-check-label" for="formCheck-1">Label</label>
          </div>
        </li>
        <li class="list-group-item">
          <div class="form-check">
            <input
              class="form-check-input"
              type="checkbox"
              id="formCheck-2"
            /><label class="form-check-label" for="formCheck-2">Label</label>
          </div>
        </li>
        <li class="list-group-item">
          <div class="form-check">
            <input
              class="form-check-input"
              type="checkbox"
              id="formCheck-3"
            /><label class="form-check-label" for="formCheck-3">Label</label>
          </div>
        </li>
      </ul>
      <div class="input-group mt-3 mb-3">
        <input
          class="form-control"
          type="text"
          placeholder="Add a new thing to do here..."
          style="border-top-left-radius: 1em; border-bottom-left-radius: 1em"
        /><button
          class="btn btn-primary"
          type="button"
          style="border-top-right-radius: 1em; border-bottom-right-radius: 1em"
        >
          <i class="fas fa-plus me-2"></i>Add
        </button>
      </div>
      <div class="form-check ps-4 ms-3">
        <input
          class="form-check-input"
          type="checkbox"
          id="formCheck-4"
        /><label class="form-check-label" for="formCheck-4"
          >Show completed items?</label
        >
      </div>
    </div>
  </div>
</template>

<script>
// import HelloWorld from "./components/HelloWorld.vue";

export default {
  name: "App",
  components: {
    // HelloWorld,
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
