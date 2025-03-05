<template>
<div id="testing">
    <p>Type Somthing</p>
    <i>Press Enter</i>
    <br/>
    <form v-on:submit.prevent>
        <input v-on:keypress="submit" type="text" v-model="name">
    </form>
    <ul>
        <li v-for="(item,index) in data" v-bind:key="index">
        <span>{{item}}</span>
        <a v-on:click.prevent="deleteItem(index)">Delete</a>

        <a v-on:click.prevent="editItem(index)">Edit</a>
        </li>
    </ul>

</div>
</template>
<script>
import Vue from 'vue'
export default{
    name:"test-tenth",
    data:()=>{
        return{
            name:"",
            data:[],
            editIndex:false,
        }
    },
    methods:{
        submit:function(e){
            if(e.keyCode===13){
             if(this.editIndex){
                Vue.set(this.data,this.editIndex,this.name);
                this.name="";
                this.editIndex=-1
             }
             else{
                this.data.push(this.name);
                this.name="";
             }
            }
        },
        deleteItem:function(index){
            this.data.splice(index,1)
        },
        editItem:function(index){
            this.editIndex=index;
            this.name=this.data[index]
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
#testing li a{
    font-size:10px;
    float:right;
    padding:5px
}
</style>