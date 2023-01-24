<template>

    <div class="container-fluid">
      <h1 class="mt-4 mb-4">Todo List</h1>
      <!-- <p>{{ todos }}</p> -->
      <ul v-for="todo in todos" :key="todo.name" class="list-group" >
        <li class="list-group-item">
          <div class="form-check">
            <input class="form-check-input" type="checkbox" id="formCheck-1" v-model="todo.done" /><label class="form-check-label" for="formCheck-1">{{ todo.text }}</label>
          </div>
        </li>
      </ul>
      <div class="input-group mt-3 mb-3">
        <input class="form-control" type="text" placeholder="Add a new thing to do here..." style="border-top-left-radius: 1em; border-bottom-left-radius: 1em" /><button class="btn btn-primary"
          type="button" style="border-top-right-radius: 1em; border-bottom-right-radius: 1em">
          <i class="fas fa-plus me-2"></i>Add
        </button>
      </div>
      <div class="form-check ps-4 ms-3">
        <input class="form-check-input" type="checkbox" id="formCheck-4" /><label class="form-check-label" for="formCheck-4">Show completed items?</label>
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

    },
    computed: {

    }
}


</script>

<style scoped>
  .to-do-list {

  }
</style>
