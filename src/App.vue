<template>
  <div id="app">
    <div id='cover'></div>
    <Todo></Todo>
  </div>
</template>

<script>
import Todo from './todo/todo.vue'
export default {
  name: 'App',
  components:{
    Todo
  }
}
</script>

<style>
#app {
  position: absolute;
  left: 0;
  right: 0;
  top:0;
  bottom:0;
}
#cover{
  position: absolute;
  left: 0;
  top:0;
  right: 0;
  bottom: 0;
  background-color: #BDFCC9;
  opacity: 0.7;
  z-index: -1;
}
</style>
