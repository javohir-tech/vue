<script>
    export default{
        data(){
            return {
                counter : 0
            }
        },
        methods:{
            onIncrement(){
                this.counter += 1;
            },
            onDecrement (){
                if(this.counter > 0){
                    this.counter -= 1;
                }
            }
        }
    }
</script>

<template>
    <div>
        <h1>Counter : {{ counter }}</h1>
        <button @click="onIncrement">add</button>
        <button @click="onDecrement">delete</button>
    </div>
</template>

<style>

</style>