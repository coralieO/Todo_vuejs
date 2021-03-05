
<template>
  <div id="app">
     <section class="hero is-warning is-bold is-fullheight">
      <div class="hero-body">
        <div class="container has-text-centered" >
          <section id="todo">
            <!-- <router-link :to="{ path: 'about' }"><a href="about"></a> </router-link> -->
          <todo-card></todo-card>
          </section>
          
        </div>
      </div>

      <div class="hero-foot">
        <div class="container">
          <div class="content has-text-centered pb-5">
            <p>
              <strong>Atelier Mars 2021</strong>
            </p>
            <section>
              
            </section>
            <p>
              Découvrez comment styliser simplement votre ToDo list avec 
              <a class="has-text-primary" href="https://bulma.io/">
                <strong>Bulma</strong>
              </a> 
            </p>
          </div>
        </div>
      </div>
    </section>
  </div>
</template>

<script>


import TodoCard from './components/TodoCard.vue'
// import About from './components/about.vue'
export default {
  name: 'app',
  components:{
    TodoCard
    // About
  },
  data () {
    return {
      msg: 'Hello, et bienvenue sur la demo TodoList en Vue.js!'
    }
  }
}
</script>

<style>
#todo{
  background-color: azure;
  height: 80vh;
}
</style>