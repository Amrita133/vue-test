<template>
    <div id="testing">
        {{name}} testing
        <br/>
        <br/>
        <input type="text" v-model="name">
        <button v-on:click="clear">Clear</button>
        <button v-on:click="makeCapital">Caps</button>
    </div>
</template>>
<script>
    export default{
        name:"Test-fourth",
        data:()=>{
            return{
                name:"Amrita"
            }
        },
        created:function(){
            console.log("created")
        },
        mounted:function(){
            console.log("mounted")
        },
        updated:function(){
            console.log("updated")
        },
        destroyed:function(){
            console.log("destroyed")
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