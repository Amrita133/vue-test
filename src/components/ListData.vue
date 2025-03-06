<template>
  <div id="list">
    
    <FormData v-on:submit-item="submit" />


    <ul>
      <li v-for="(item, index) in data" :key="index">
        <span>{{ item }}</span>
        
        <a @click="edit(index)">Edit</a>
        <a @click="deleteItem(index)">Delete</a>
        
      </li>
    </ul>
  </div>
</template>

<script>
import FormData from './FormData.vue';

export default {
  name: "ListData",
  components: {
    FormData
  },
  data() {
    return {
      data: [], 
      editIndex: -1, 
      name: "" 
    };
  },
  methods: {
    submit(name) {
      if (name.trim()) {
        this.data.push(name);
      }
    },
    edit(index) {
      this.name = this.data[index];
      this.editIndex = index;        
    },
    saveEdit() {
      if (this.editIndex !== -1) {
        this.data[this.editIndex] = this.name;
        this.editIndex = -1; 
        this.name = ""; 
      }
    },
    deleteItem(index) {
      this.data.splice(index, 1); 
    }
  }
};
</script>
<style>
#list li{
    padding: 10px 20px;
    border: 1px solid black;
    border-radius: 5px;
    align-items: center;
}
#list li a{
    font-size: 12px;
    float:right;
    color: gray;

}

</style>
