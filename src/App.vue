<script>
    export default {
        data(){
            return {
                counter : 0
            }
        },
        methods:{
            inCrements(){
                this.counter += 1;
            },
            inDecrement(){
               if(this.counter >0){
                this.counter -=1;
               }
            }
        }
    }
</script>

<template>
    <div>
         <h1>Counter : {{counter}} </h1>
         <div>
            <button @click="inCrements">add</button>
            <button @click="inDecrement">delete</button>
         </div>
    </div>
</template>

<style>

</style>