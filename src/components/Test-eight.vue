<template>
  <div id="testing">
    <div :style="{ color: color_value }">
      {{ name }} Testing
    </div>
    <br />
    <input type="text" v-model="name" />
    <select v-model="color_value">
      <option v-for="(col, index) in colors" :key="index" :value="col">
        {{ col }}
      </option>
    </select>
  </div>
</template>

<script>
export default {
  name: "TestEight",
  data() {
    return {
      name: "Amrita",
      colors: ["red", "pink", "blue", "orange"],
      color_value: "black", 
    };
  },
};
</script>

<style>

</style>
