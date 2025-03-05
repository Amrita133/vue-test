<template>
    <div id="testing">
      
        <div :class="{red:isRed}">
            {{name}}Testing

        </div>
        <br/>
        <br/>
        {{date}}
        <br/>
        <input type="text" v-model="name">
        <button v-on:click="clear">Clear</button>
        <button v-on:click="makeCapital">Caps</button>
        <input :checked="isRed" v-model="isRed" type="checkbox" @click="red"/>
        RED
    </div>
</template>
<script>
  export default{
    name:"Test-sixth",
    data:()=>{
        return{
            name:"Amrita",
            date:false,
            isRed:false,

        }
    },
    created:function(){
        console.log("created");
        this.date=new Date().getFullYear()+"-"+new Date().getMonth()+"-"+new Date().getDay();
    },
    mounted:function(){
        console.log("mounted");
        this.date=new Date().getFullYear()+"-"+new Date().getMonth()+"-"+new Date().getDay();
    },

    methods:{
        clear:function(){
            this.name="";
        },
        makeCapital:function(){
            this.name=this.name.toUpperCase()
        },
        red:function(){
            console.log(this.isRed)
        }
    }
    

  }
</script>
<style>
.red{
    color: red;
}
.green{
    color: green;
}
</style>

