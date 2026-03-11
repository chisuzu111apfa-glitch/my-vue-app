<script setup>
import { ref, computed } from 'vue'

const score = ref(0)
const evaluation = computed(() => {
  return score.value >= 60 ? '合格' : '不合格'
})
</script>

<template>
  <p>{{ evaluation }}</p>
  <input v-model="score" type="number" />
</template>

<style>
.container {
  padding: 20px;
}
input {
  display: block;
  margin-bottom: 10px;
  padding: 5px;
}
</style>
