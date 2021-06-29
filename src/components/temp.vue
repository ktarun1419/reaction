<template>
    <div>
        <p v-html="rowhtml"></p>
        
        <h2>{{name}}</h2>
        <button v-on:click="us">click</button>
        <h3>{{ok?"yes":"no"}}</h3>
        </div>
</template>
<script>
export default {
    name:'temp',
    data(){
        return{
            name:'tarun',
            age:19,
            ok:true,
            rowhtml:"<h1>TEMPLATES IN VUE</h1>"
        }
    },methods:{
        us(){
            this.name='khoobayshee'
        }
    }
}
</script>