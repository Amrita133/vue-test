<template>
    <div id="testing">
        <div v-bind:style="{color:color_value.color}">
            {{name}} Testing

        </div>
        <br/>
        <br/>
    
        <br>
        <input type="text" v-model="name"/>
        <button v-on:click="clear">Clear</button>
        <select v-model="color_value">
            <option v-bind:value="{color:'red'}">red</option>
            <option v-bind:value="{color:'yellow'}">yellow</option>
            <option v-bind:value="{color:'blue'}">blue</option>
            <option v-bind:value="{color:'orange'}">orange</option>  

        </select>
      

    </div>
</template>
<script>
export default{
    name:"Test-seven",
    data:()=>{
        return{
            name:"Amrita",
            color_value:{
                color:"black"
            },

        }
    },
    methods:{
        clear:function(){
            this.name="";
        },
  
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