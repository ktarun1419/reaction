<template>
  <div class="black" v-if="showblock" v-on:click="stoptimer">
      click to start game</div>
</template>

<script>
export default {
    name:'block',
    props:['delay'],
    data(){
        return{
            showblock:false,
            timer:null,
            reactiontime:0,
        }
    },mounted(){
        setTimeout(() => {
            this.showblock=true
            this.starttimer()
            
        }, this.delay);
    
    },methods:{
        starttimer(){
            this.timer=setInterval(() => {
                this.reactiontime+=10
                
            }, 10);

        },stoptimer(){
            clearInterval(this.timer)
            this.$emit('end',this.reactiontime)

        }
    }

    

}
</script>

<style>
.black{
    width: 400px;
    background-color: darkgreen;
    color: white;
    text-align: center;
    padding: 100px 0;
    margin: 40px auto;
    border-radius: 20px;
}

</style>