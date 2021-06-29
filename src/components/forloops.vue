<template>
    <div>
        <h1 class="div">HELLO EVERYONE!!!!</h1>
        <h2 v-bind:class="{display:tarun}">CLASS BINDING WITH OBJET</h2>
        <button v-on:click="change">Colour change</button>
    
    </div>
</template>
<script>
export default {
    name:'forloops',
    data(){
        return {
            tarun:false
        }
    },methods:{
        change(){
            this.tarun=!this.tarun
        }
    }
   
        
    
}
</script>
<style scoped>
div{
    color:rgb(255, 0, 0);
    font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 'Open Sans', 'Helvetica Neue', sans-serif;
    text-align: center;

}.display{
    color: darkblue;
}
</style>