<template>
    <div id="testing">
        {{name}}Testing
        <br/>
        <br/>
        {{date}}
        <br>
        <input type="text" v-model="name"/>
        <button v-on:click="clear">Clear</button>
        <button v-on:click="makeCapital">Caps</button>
    </div>
</template>
<script>
export default {
    name:"Test-fifth",
    data:()=>{
        return{
            name:"Amrita",
            date:false
        }
},
created:function(){
    console.log("created");
    this.date=new Date();
},
mounted:function(){
    console.log("mounted");
    this.date=new Date();
},
updated:function(){
    console.log("updated");
},
destroyed:function(){
    console.log("destroyed")
    this.message=new Date();
},
methods:{
    clear:function(){
        this.name=""
    },
    makeCapital:function(){
        this.name=this.name.toUpperCase()
    }
}


}
</script>
<style>
</style>