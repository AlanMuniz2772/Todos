<template>
    <div>
        <div v-bind:key="todo.id" v-for="todo in todoslist">
            <TodoItem v-bind:todo = "todo" v-on:delete-todo="$emit('delete-todo', todo.id)" 
            v-on:change-todo="$emit('change-todo', todo.id)"/>
        </div>
    </div>
</template>

<script>
import TodoItem from './TodoItem.vue';
    export default {
        name: 'TodosIn',
        props: ['todoslist'],
        components: {TodoItem},
        methods:{
            change(todoCompleted){
                console.log(todoCompleted);
            }
        }
    }
</script>

<style></style>