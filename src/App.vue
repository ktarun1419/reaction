<template>
  <div id="app">
    <!--<img alt="Vue logo" src="./assets/logo.png">
    {{users.firstname}}
    {{users.username}}
    <button v-on:click="hello">create new account</button>
    <home />
    <forloops />
    <temp />
    <databinding v-bind:header="header" theme="sale">
      <template v-slt:links>
        <a href="http://youtube.com">for  more info</a>
      </template>
      <h1>esting slots</h1>
    </databinding>-->
    <h1>NINJA REACTION TIMER</h1>
    <reactiontimer   v-if="showresult" v-bind:score="this.score"/>
    <button v-on:click="play"  v-bind:disabled="isplay">start</button>
    <block v-if="isplay" v-bind:delay="delay" @end="endGame" />
    
    
    
    

  </div>
</template>

<script>
import Block from './components/block.vue';
/*import home from'./components/home.vue' ;
import forloops from "./components/forloops.vue";
import temp from "./components/temp.vue";
import databinding from "./components/databinding.vue";*/
import reactiontimer from "./components/reactiontimer.vue";
export default {
  name: 'App',
  components:{
   /* home,
    forloops,
    temp,
    databinding,*/
    reactiontimer,
    Block


  },methods:{
    hello(){
      document.write("welcome to Twotter")

    },play(){
      this.isplay=true
      this.delay=Math.random()*5000
      console.log(this.delay)
      this.showresult=false

    },endGame(reactiontime){
      this.score=reactiontime
      this.isplay=false
      this.showresult=true

    }
    },data(){
    return{
      header:"signup and grab rewards",
      isplay:false,
      delay:null,
      score:null,
      showresult:false
    }
  }
}
  

</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: yellowgreen;
  margin: 21px;
  height: 400px;
  background-color:rgb(25, 25, 109);
}

</style>
