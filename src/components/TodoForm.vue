<template>
<div id="todoForm">
  <input type="text" v-model="todo">
  <button @click="submitForm">Submit</button>
</div>
</template>

<script>
export default {
    data(){
        return{
            todo:null
        }
    },
    methods:{
        submitForm(){
            this.$emit("list",this.todo);
            this.todo=null;
        }
    }
}
</script>

<style>

</style>