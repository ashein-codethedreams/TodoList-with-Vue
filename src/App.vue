<template>
  <div id="app">
    <app-todo-form @list="addTodo" />
    <app-todo-list :items="todos"/>
    <p>Todo size from App:{{todos.length}}</p>
  </div>
</template>

<script>

import TodoFrom from "@/components/TodoForm.vue"
import TodoList from "@/components/TodoList.vue"

export default {
  name: 'App',
  components:{
     "app-todo-form":TodoFrom,
     "app-todo-list":TodoList
  },
  data(){
    return{
      todos:["Do my homework","Clean my room"]
    }
  },
  methods:{
           addTodo(data){
               this.todos.push(data);
           }
       }
}
</script>

<style>

</style>
