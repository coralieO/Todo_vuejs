<template>
    <div class="items" >
            <ul>
              <li><input type="checkbox" name="" id=""></li>
              <li>{{name}}</li>
                <li>
                    <div class="actions">
                          <i class="fas fa-trash-alt"></i>
                    </div>  
                </li>
            </ul>
        </div>
</template>


<script>



export default {
  name: 'todo-list',
  props: {
    name: String,
    completed: Boolean
  }
}
</script>
<style>
.items ul{
  padding-top: 40px;
  display: flex;
}
</style>
