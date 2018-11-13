<template>
    <div>
        <!-- Javascript excpressions in Vue are enclose in double curly brackets -->
        <p>Completed Tasks {{ todos.filter( todo => {return todo.done === true}).length }}</p>
        <p>Pending Tasks: {{ todos.filter( todo => {return todo.done === false}).length }}</p>
        <!-- Passing the Data to the component -->
        <todo v-for="todo in todos"  v-bind:todo="todo" v-bind:key="todo"> </todo>

      
    </div>
</template>
<script>

import Todo from "./Todo";


export default {
    props: ['todos'],
    components: {
        Todo,
    }
}
</script>
<style>

</style>

