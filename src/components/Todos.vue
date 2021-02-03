<template>
    <div >
       <div class="list-group text-start">
            <TodoItem
                v-bind:key="todo.id" 
                v-for="todo in todos" 
                v-bind:todo="todo" 
                v-on:markAsComplete="$emit('markAsComplete',todo.id)"
                v-on:delItem="$emit('delItem',todo.id)"
            />
       </div>
    </div>
</template>

<script>
import TodoItem from "./TodoItem"

export default {
    name: "Todos",
    props:['todos'],
    components:{
        TodoItem
    },
    methods:{
       
    }
}
</script>

<style scoped>

</style>