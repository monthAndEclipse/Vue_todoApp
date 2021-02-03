<template>
    <div>
        
        <a  href="#" 
                class="list-group-item list-group-item-action " 
                aria-current="true"
                v-bind:class="{'is-completed':todo.isCompleted}"
        >
            <div class="container-fulid">
                <div class="row justify-content-between">
                    <div class="col-4">
                        <input class="m-1" type="checkbox" v-on:change="$emit('markAsComplete',todo.id)"> {{todo.title}}
                    </div>
                    <div class="col-1 text-end">
                        <button 
                            type="button" 
                            class="btn btn-danger rounded-circle"
                            v-on:click="$emit('delItem',todo.id)"
                        >
                        X
                        </button>
                    </div>
                </div>
              
            </div>
               
        </a>
        
    </div> 
</template>


<script>
export default {
    name:"TodoItem",
    props:['todo'],
    methods:{
       
    }
}
</script>


<style scoped>
 .is-completed{
     text-decoration: line-through;
 }
</style>