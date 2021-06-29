<template>
    <div>
        <h1 class="rs" v-if="fun">{{header}}</h1>
        <button v-on:click.alt="open">grab rewards</button>
        <p style="white-space:pre-line">{{message}}</p>
        <textarea  v-model="message"></textarea>
        <slot></slot>
        
        </div>
        
</template>
<script>
export default {
    name:'databinding',
    props:['header','theme'],
    data(){
        return{
            kar:true,
            message:"hi tarun",
            fun:true

        }
    },methods:{
        open(){
            this.fun=!this.fun

        }
    }
    }

</script>
<style scoped>
.rs{
    color: white;
    border: darkgreen;
    background-color: red;
    font-style: oblique;
    font-family: Georgia, 'Times New Roman', Times, serif;
    font-size: 30px;
}
</style>