<script setup>
import { ref } from "vue";
const seedPhrase = ref("You enter a room");
const numberToGenerate = ref(1);
const buttonText = ref("Generate 1 sentence");
function updateButtonText() {
  if (numberToGenerate.value === 1) buttonText.value = "Generate 1 sentence";
  else buttonText.value = "Generate " + numberToGenerate.value + " sentences";
  return buttonText;
}

function callAPI() {
  console.log("placeholder");
  console.log("Button was clicked");
  console.log("Seed Phrase was: " + seedPhrase.value);
}
</script>

<template>
  <div class="item">
    <div class="details">
      <label>
        Enter a seed phrase.
        <input v-model="seedPhrase" />
      </label>
    </div>

    <div class="details">
      <span>Number of setences to generate: </span>
      <select v-model="numberToGenerate" @change="updateButtonText">
        <option disabled value="Please select one"></option>
        <option>1</option>
        <option>2</option>
        <option>3</option>
        <option>4</option>
        <option>5</option>
        <option>6</option>
        <option>7</option>
        <option>8</option>
        <option>9</option>
        <option>10</option>
      </select>
    </div>
    <div class="details">
      <div class="generatorButton">
        <button @click="callAPI">{{ buttonText }}</button>
      </div>
    </div>
  </div>
</template>

<style scoped>
button {
  margin-top: 2rem;
  color: blue;
}
</style>
