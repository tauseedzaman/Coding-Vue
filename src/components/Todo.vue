<template>
  <h1 class="text-light">Just Test Todo App</h1>
  <div class="col-md-6 mx-auto sticky-top" id="todo-list-example">
    <form class="form" v-on:submit.prevent="addNewTodo">
      <div class="form-group shadow-lg  border-success rounded">
        <label for="new-todo text-light">Add a todo</label>
        <input
          class="form-control"
          v-model="newTodoText"
          id="new-todo"
          placeholder="Todo Message"
        />
      </div>
      <button class="btn btn-success btn-block mb-4">Add Todo</button>
    </form>
    
  </div>
  <hr>
  
  <div class="col-md-8 mx-auto">
      <h3 class="text-light">All Todos</h3>
      <ol>
        <p class="text-danger" v-if="todos.length == 0">No Todo Found!</p>
      <li class=" bg-light shadow border rounded my-1 p-3" v-else v-for="(todo, i) in todos" :key="todo.id" :title="todo.title">
        {{ todo.title }}
        <button
          v-on:click="todos.splice(i, 1)"
          class="btn btn-danger btn-sm float-right" title="delete this item"
        >
          X
        </button>
      </li>
    </ol>
  </div>
</template>

<script>
export default {
  data() {
    return {
      newTodoText: "",
      todos: [
        {
          id: 1,
          title: "You Need To Learn Vue Right Now!!!",
        },
      ],
      nextTodoId: 2,
    };
  },
  methods: {
    addNewTodo() {
      if(this.newTodoText == ''){
        alert("Empty Todo.....");
        return 0;
      }
      this.todos.push({
        id: this.nextTodoId++,
        title: this.newTodoText,
      });
      this.newTodoText = "";
    },
    },
};
</script>

<style>
</style>