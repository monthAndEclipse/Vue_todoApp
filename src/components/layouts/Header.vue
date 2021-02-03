<template>
    <div class="bg-dark text-white">
        <h1 >Todo List</h1>
        <div id="nav"> 
            <router-link  class="text-white" to="/">Home</router-link> |
            <router-link  class="text-white" to="/about">About</router-link>
        </div>
    </div>
</template>

<script>
export default {
    name:"Header"
}
</script>

<style scoped>
h1{
    margin-bottom: 0;
}
a{
    text-decoration: none;
}
a:hover{
     text-decoration: underline;
}
</style>