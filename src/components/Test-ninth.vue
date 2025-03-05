<template>
<div id="testing">
    <p>Type Somthing...</p>
    <i>Press Enter</i>
    <br/>
    <form v-on:submit.prevent>
        <input v-on:keypress="submit" type="text" v-model="name"/>
    </form>
    <ul>
        <li v-for="(item,index) in data" v-bind:key="index">{{item}}</li>
    </ul>
</div>
</template>
<script>
export default {
    name:"Test-ninth",
    data:()=>{
        return{
            name:"",
            data:[]
        }
    },
    methods:{
        submit:function(e){
            if(e.key==="Enter"){
                this.data.push(this.name);
                this.name="";
            }

        }
    }
}
</script>
<style>
#testing li{
    border:1px solid black;
    padding:5px;
    margin:5px;
    border-radius:5px
}
</style>