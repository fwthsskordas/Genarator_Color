<script setup>
import { ref } from 'vue';  

const red = ref(0);
const blue = ref(0);
const green = ref(0);
</script>

<template>
  <main :style="{backgroundColor: `rgb(${red}, ${green}, ${blue})`}">
    <div class="container">
      <input type="number" v-model="red" placeholder="red">
      <input type="number" v-model="blue" placeholder="blue">
      <input type="number" v-model="green" placeholder="green">
    </div>
  </main>
</template>

<style scoped>
main{
  background-color: rgb(122, 50, 75);
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