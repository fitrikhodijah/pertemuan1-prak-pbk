<script setup>
// Import komponen utama
import HelloWorld from './components/HelloWorld.vue'
import { ref } from 'vue'

// Menambahkan state untuk menghitung klik
const clickCount = ref(0)

// Fungsi untuk menangani klik
const incrementClick = () => {
  clickCount.value++
}
</script>

<template>
  <div class="app-container">
    <a href="https://vite.dev" target="_blank">
      <img src="/vite.svg" class="logo" alt="Vite logo" />
    </a>
    <a href="https://vuejs.org/" target="_blank">
      <img src="./assets/vue.svg" class="logo vue" alt="Vue logo" />
    </a>

    <HelloWorld msg="Vite + Vue" />

    <div class="click-counter">
      <p>Jumlah klik: {{ clickCount }}</p>
      <button @click="incrementClick">Klik saya!</button>
    </div>
  </div>
</template>

<style scoped>
.app-container {
  text-align: center;
  margin-top: 2rem;
}

.logo {
  height: 6em;
  padding: 1.5em;
  will-change: filter;
  transition: filter 300ms;
}

.logo:hover {
  filter: drop-shadow(0 0 2em #646cffaa);
}

.logo.vue:hover {
  filter: drop-shadow(0 0 2em #42b883aa);
}

.click-counter {
  margin-top: 2rem;
}

button {
  padding: 0.5rem 1rem;
  font-size: 1rem;
  cursor: pointer;
  border: none;
  border-radius: 0.5rem;
  background-color: #42b883;
  color: white;
  transition: background-color 0.3s;
}

button:hover {
  background-color: #35495e;
}
</style>
