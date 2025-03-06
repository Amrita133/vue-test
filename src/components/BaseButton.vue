<template>
  <button 
    :style="{ backgroundColor: backgroundColor, color: textColor }" @click="$emit('button-click')" class="base-button" >
    {{ text }}
  </button>
</template>

<script>
export default {
  props: {
    text: {
      type: String,
      default: "Click Me"
    },
    backgroundColor: {
      type: String,
      default: "#0069D9"
    },
    textColor: {
      type: String,
      default: "#FFFFFF"
    }
  }
};
</script>

<style scoped>
.base-button {
  margin-top: 25%;
  margin-left:5px;   
  padding: 10px 20px;
  font-size: 16px;
  border: none;
  border-radius: 5px;
  cursor: pointer;
}
</style>
