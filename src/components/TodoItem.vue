<template>
  <p :class="['todo-item', todoProps.completed?'is-completed':'']">
    <input type="checkbox" v-on:change="markItemCompleted"/>
    {{todoProps.title}}
    <button class="del-btn">Delete</button>
  </p>
</template>

<script>
// import { ref } from 'vue';

export default {
    name : "TodoItem",
    props: ['todoProps'],
    setup() {
        const markItemCompleted = () => {
            todoProps.
            console.log("Marked");
        }
        return {
            markItemCompleted
        }
    }
}
</script>

<style>
.todo-item {
    background: #f4f4f4;
    padding: 10px;
    margin: 0;
    border-bottom: 1px #ccc dotted;
}
.del-btn {
    background: #f00;
    color: #fff;
    border: none;
    cursor: pointer;
    float:right;
}
.is-completed {
    text-decoration: line-through;
}
</style>