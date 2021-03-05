<template>
<div>
<header>
<nav class="menu">
      <ul>
        <li class="vert">{{currentDateTime()}}</li>
        <li>{{title}}</li>
        <li class="vert">{{tasks.length}} tâches</li>
      </ul>
  </nav>

</header>
  <new-todo v-on:sendTask="addTask($event)"/>  <ul v-for="items in tasks" v-bind:key="tasks.indexOf(items)">
    <todo-list  v-bind:tasks="items.name"></todo-list> </ul>

</div>


 
</template>

<script>
import NewTodo from './NewTodo.vue'
import TodoList from './TodoList.vue'
  export default{
    name: 'todo-card',
    components:{
      NewTodo,
      TodoList
   },
    
    data() {
      return { title: 'VueJs Tutorial Todo List', tasks: []}
    },
     methods: {
      currentDateTime(){
      const timeElapsed = Date.now();
      const today = new Date(timeElapsed);
      const date = today.toDateString()
      return date;
      },
      addTask(tasks){
         this.tasks.push({name: tasks, completed:false})
      }
    },
   
    }

</script>

<style>
nav{
  height: 10vh;
  border-bottom: black solid 1px;
  padding-top: 30px;
  margin-bottom: 30px;
}
nav ul{
display: flex;
  justify-content: space-around;
}
.vert{
  color: rgb(87, 228, 228);
}
</style>