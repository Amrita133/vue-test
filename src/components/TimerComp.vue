<template>
<div id="timer">
<h2>Count-Up Timer</h2>
<counter-comp :time="timeElapsed"/>
<button @click="startTimer" :disabled="isRunning">Start</button>
<button @click="stopTimer" :disabled="!isRunning">Stop</button>
</div>
</template>

<script>
import CounterComp from './CounterComp.vue'
export default{
    components:{
       CounterComp  
    },
    data:()=>{
        return{
        timeElapsed:0,
        isRunning:false,
        timer:null
        }
    },
    methods:{
        startTimer:function(){
            if(!this.isRunning){
                this.isRunning=true;
                this.timer=setInterval(
                    ()=>{
                        this.timeElapsed++;
                    },1000)
            }
        },
        stopTimer:function(){
            this.isRunning=false;
            clearInterval(this.timer)
        }
    }
}
</script>
<style>
.timer{
    text-align: center;
}
button{
    padding: 5px 10px;
    margin:5px;
    cursor: pointer;
    font-size: 12px;
}
</style>