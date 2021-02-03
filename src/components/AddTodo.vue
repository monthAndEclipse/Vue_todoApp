<template>
    <div>
        <form @submit="addTodo">
            <div class="input-group">
                <input
                    type="text" 
                    class="form-control w-75" 
                    placeholder="add Todo..." 
                    aria-describedby="emailHelp"
                    v-model="title"
                >
                <button type="submit" class="btn btn-primary ">Submit</button>
            </div>
        </form>
    </div>
</template>

<script>
// import { v4 as uuidv4 } from 'uuid';
export default {
    name:"AddTodo",
    data(){
        return {
            title:''
        }
    },
    methods:{
        addTodo(e){
           e.preventDefault();
            const newTodo =  {
                title:this.title,
                // id:uuidv4(),
                isCompleted:false
            }
            //send up to parent
            this.$emit('addTodo',newTodo);
            this.title=""
        }
    }
}
</script>

<style scoped>

</style>