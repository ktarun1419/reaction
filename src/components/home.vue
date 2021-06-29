<template>
<div>
    <h1 v-if="show" style="color:blue;">hello To Twotter</h1>
    <button v-on:click="display">Toggle element</button></div>
</template>
<script>
export default{
    name:'home',
    
    data(){
        return {show:true}
    },methods:{
        display(){
            this.show=!this.show
        }
    }
}
</script>
