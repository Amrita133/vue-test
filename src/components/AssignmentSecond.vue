

<template>
  <div>
    <base-button text="Primary" backgroundColor="#0069D9" textColor="#ffffff" @button-click="showAlert" />
    
    <base-button :text="ReverseMe" backgroundColor="#218838" textColor="#FFFFFF" @button-click="toggleText"/>
    {{buttonText}}
  </div>
</template>

<script>
import BaseButton from './BaseButton.vue';

export default {
  components: {
    BaseButton
  },
  data() {
    return {
      buttonText: "Reverse the word"
    };
  },
  methods: {
    showAlert() {
      alert("Button clicked!");
    },
    toggleText() {
      this.buttonText=this.buttonText.split("").reverse().join("");
    }
  }
};
</script>

