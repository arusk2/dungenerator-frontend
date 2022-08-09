<script setup>
import { ref } from "vue";
import axios from "axios";
var seedPhrase = ref("You enter a room");
var numberToGenerate = ref(1);
var buttonText = ref("Generate 1 sentence");
//var apiReturn = ref(Object);
const apiThinkingText = ref(["Generating..."]);
//var apiThinkingFlag = ref(false);
var generated_text = ref(["What will you generate?"]);
const apiURL =
  "https://s99cwqgkyk.execute-api.us-west-2.amazonaws.com/prod-v1-0/make-inference";

function updateButtonText() {
  if (numberToGenerate.value === 1) buttonText.value = "Generate 1 sentence";
  else buttonText.value = "Generate " + numberToGenerate.value + " sentences";
  return buttonText;
}

function callAPI() {
  generated_text.value = apiThinkingText.value;
  axios
    .post(
      apiURL,
      {
        params: {
          input: seedPhrase.value,
          num_return_sequences: parseInt(numberToGenerate.value, 10),
        },
      },
      { headers: { "content-type": "application/json" } }
    )
    .then((response) => {
      var body = JSON.parse(response.data.body);
      var text = [];
      for (var i = 0; i < numberToGenerate.value; i++) {
        text.push(body[i]);
      }
      generated_text.value = text;
    })
    .catch((error) => {
      console.error("An error occured.", error);
    });
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
    <div class="item">
      <div class="return-box">
        <ul class="no-bullets">
          <li v-for="item in generated_text" :key="item.id">
            {{ item }}
          </li>
        </ul>
      </div>
    </div>
  </div>
</template>

<style scoped>
button {
  margin-top: 2rem;
}
.return-box {
  margin: 20px 0px;
  overflow-y: scroll;
  border: 4px double #4b4c53;
  background-color: #efeff3;
  min-height: 100px;
  max-height: 150px;
  height: 30vh;
}
ul.no-bullets {
  list-style-type: none;
  padding: 8px;
}
</style>
