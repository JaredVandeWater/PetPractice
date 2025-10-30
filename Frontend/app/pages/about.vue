<template>
  <div class="counter-page">
    <h1>Nuxt Counter Example</h1>
    <p class="count-display">Count: {{ count }}</p>
    <button class="count-button" @click="increment">Add +1</button>
  </div>
</template>

<script setup>
import { ref } from "vue";

const count = ref(0);

function increment() {
  count.value++;
}
</script>

<style lang="scss" scoped>
.counter-page {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  min-height: 100vh;
  background: linear-gradient(135deg, #f9fafb, #e5e7eb);
  color: #333;
  font-family: "Inter", sans-serif;

  h1 {
    font-size: 2rem;
    margin-bottom: 1rem;
    color: #222;
  }

  .count-display {
    font-size: 1.5rem;
    margin-bottom: 1.5rem;
    font-weight: bold;
  }

  .count-button {
    background-color: #0070f3;
    color: white;
    border: none;
    border-radius: 8px;
    padding: 0.75rem 1.5rem;
    font-size: 1rem;
    cursor: pointer;
    transition: background-color 0.2s, transform 0.1s ease-in-out;

    &:hover {
      background-color: #0059c1;
    }

    &:active {
      transform: scale(0.97);
    }
  }
}
</style>
