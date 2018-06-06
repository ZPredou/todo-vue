<template>
  <div>
    <p>Taches éfféctués :{{todos.filter(todo => {return todo.done === true}).length}}</p>
    <p>Taches en cours :{{todos.filter(todo => {return todo.done === false}).length}}</p>
    <todo :key="todo.id" v-for="todo in todos" v-bind:todo="todo"></todo>
  </div>
</template>

<script type = "text/javascript" >

import Todo from './Todo';

export default {
  props: ['todos'],
  components: {
    Todo,
  },
};
</script>