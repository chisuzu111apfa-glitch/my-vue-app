<script setup>
import { ref } from 'vue'
const isRed = ref(true)
const isBlue = ref(true)
function toggleRed() {
  isRed.value = !isRed.value
}
function toggleBlue() {
  isBlue.value = !isBlue.value
}
</script>

<template>
  <div :class="{ red: isRed, container: isBlue }">Hello World</div>
  <button @click="toggleRed">Toggle Red</button>
  <button @click="toggleBlue">Toggle Blue</button>
</template>

<style>
.red {
  color: red;
}
.container {
  background-color: blue;
}
</style>
