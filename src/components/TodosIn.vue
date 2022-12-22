<template>
    <div>
        <div v-bind:key="todo.id" v-for="todo in todoslist">
            <div>{{todo.title}}</div>
        </div>
    </div>
</template>

<script>
    export default {
        name: 'TodosIn',
        props: ['todoslist']
    }
</script>

<style></style>