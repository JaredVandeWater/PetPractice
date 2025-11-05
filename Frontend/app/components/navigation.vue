<template>
  <header>
    <nav class="">
      <NuxtLink to="/">Home</NuxtLink>
      <NuxtLink to="/about">About</NuxtLink>
    </nav>
  </header>
</template>

<script setup>
import { ref } from "vue";

const count = ref(0);

function increment() {
  count.value++;
}
</script>

<style lang="scss" scoped>
nav {
  position: fixed;
  top: 0;
  display: flex;
  background: rgb(47, 125, 186);
  color: #333;
  font-family: "Inter", sans-serif;
  padding: 2rem;
  width: 100%;
  z-index: 1000;

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
