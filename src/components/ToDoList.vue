<template>

    <div class="container-fluid">
      <h1 class="mt-4 mb-4">Todo List</h1>
      <!-- <p>{{ todos }}</p> -->
      <ul class="list-group" >
        <li class="list-group-item" v-for="(todo, index) in todos.filter(determineTodoShow)" :key="todo.name"  v-bind:class="{active: ! todo.done}">
          <div class="form-check">
            <input class="form-check-input" type="checkbox" v-bind:id="'formCheck-1' + index" v-model="todo.done" /><label class="form-check-label" for="formCheck-1">{{ todo.text }}</label>
          </div>
        </li>
      </ul>
      <form v-on:submit="handleAddTodo($event)">
        <div class="input-group mt-3 mb-3">
          <input v-model="input" class="form-control" type="text" placeholder="Add a new thing to do here..." style="border-top-left-radius: 1em; border-bottom-left-radius: 1em" />
          <button class="btn btn-primary"
            type="submit" style="border-top-right-radius: 1em; border-bottom-right-radius: 1em">
            <i class="fas fa-plus me-2"></i>Add
          </button>
        </div>
        </form>
      <div class="form-check ps-4 ms-3">
        <input class="form-check-input" type="checkbox" id="formCheck-4" v-model="showDone" /><label class="form-check-label" for="formCheck-4">Show completed items?</label>
      </div>
    </div>
</template>

<script lang="js">

  export default  {
    name: 'to-do-list',
    props: ['state'],
    mounted () {

    },
    data () {
      return this.$props.state;
    },
    methods: {
      handleAddTodo(event) {
        event.preventDefault();
        this.$data.todos.push({text:this.input, done:false});
        this.input = "";
      },
      determineTodoShow (todo) {
          if(this.$data.showDone) return true;
          return !todo.done;
      }
    },
    computed: {

    }
}


</script>

<style scoped>
  .to-do-list {

  }
</style>
