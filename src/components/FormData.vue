<template>
<div id="submitForm">
<p>Type Something</p>
<i>Press Enter</i>
<br/>
<br/>
<form v-on:submit.prevent>
<input v-on:keypress="submit" type="text" v-model="name"/>
</form>
</div>
</template>

<script>  
   export default{
    name:"FormData",
    data:()=>{
        return{
        name:"",
        editIndex:false
        }
    },
    methods:{
        submit:function(e){
            if(e.key==="Enter"){
                this.$emit("submit-item",this.name);
                this.name="";
            }
        }
    }
   }
</script>
<style>
</style>
