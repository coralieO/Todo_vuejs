<template>
<form class="newtodo is-flex" @submit.prevent="sendTask()">
<div class="input">
  <input v-model="NewTask" type="text" name="NewTask" id="new" placeholder="Ecrivez votre tâche">
  <i v-on:click="sendTask()" class="fas fa-plus-circle"></i>
</div>
</form>
</template>

<script>
  export default{
    name: 'new-todo',
    data(){
      return {
        NewTask: ""
      }
    },
    methods: {
      sendTask(){
         this.$emit("sendTask", this.NewTask)
      }
    }

  }
  
</script>

<style>
.input{
 width: 300px;
 margin: 0 auto;
}
input{
  width: 300px;
}
i{
    margin-left: 20px ;
}

</style>