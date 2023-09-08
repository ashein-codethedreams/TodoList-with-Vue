<template>
  <div id="todoList">
      <ul>
      <li v-for="(item,index) in items" :key="index"> <span @click="deleteTodo(index)" class="delete">X</span> {{index}} - {{item}}</li>
    </ul>
  </div>
</template>

<script>
export default {
   props:{items:Array},
   methods:{
     deleteTodo(index){
       this.items.splice(index,1);
     }
   }
}
</script>

<style scoped>
 .delete{
   color:red;
 }
</style>