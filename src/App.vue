<script setup>
import { reactive } from 'vue';  
import useRandom from "./Composables/useRandom"

const color = reactive({
  red: 105,
  green: 105,
  blue: 105
})


const SelectRandom = () => {
  let randomRed  = useRandom().red;
  let randomGreen= useRandom().green;
  let randomBlue = useRandom().blue;
  color.red = randomRed;
  color.green = randomGreen;
  color.blue =randomBlue;
}
</script>

<template>
  <main :style="{backgroundColor: `rgb(${color.red}, ${color.green}, ${color.blue})`}">
    <div class="container">
      <input type="number" v-model="color.red" placeholder="red">
      <input type="number" v-model="color.blue" placeholder="blue">
      <input type="number" v-model="color.green" placeholder="green">
      <button @click="SelectRandom"> Select Random Color </button>
    </div>
  </main>
</template>

<style scoped>
main{
  height: 100vh;
  display: flex;
  align-items: center;
  justify-content: center;
}

.container {
  display: flex;
  flex-direction: column;
  gap: 1rem;
  width: 200px;
}

input{
  width: 100%;
  padding: 10px;
  border-radius: 5px;
  border: 1px solid black;
  font-family: 'Courier New', Courier, monospace;
}


</style>