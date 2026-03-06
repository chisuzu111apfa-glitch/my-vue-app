<script setup>
import {ref, computed} from 'vue';

// 1. 名字と名前、それぞれのデータを用意（最初は空っぽ）
const lastName = ref('');
const firstName = ref('');

// 2. 【コンピューテッド】名字と名前を合体させた「フルネーム」を作る
const fullName = computed(() => {
  // 名字か名前、どちらかが変わるたびにここが自動で実行されます
  return lastName.value + ' ' + firstName.value;
});
</script>

<template>
  <div class="container">
    <input v-model="lastName" placeholder="名字（例：山田）" />
    <input v-model="firstName" placeholder="名前（例：太郎）" />

    <hr />

    <h2>こんにちは、{{ fullName }} さん！</h2>
  </div>
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
