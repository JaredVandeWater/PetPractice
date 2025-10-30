<script setup>
import { ref } from "vue";

// A "ref" is a reactive data source that stores a value.
// Technically, we don't need to wrap the string with ref()
// in order to display it, but we will see in the next
// example why it is needed if we ever intend to change
// the value.
const message = ref("Hello World! Home");
</script>

<template>
  <section class="hero">
    <h1>Get Local & Professional Pet Care with Winterized Yourgi</h1>
  </section>
  <h2>Discover the Benefits of Trusted Pet Care with Yourgi</h2>
  <div></div>
  <section></section>
</template>

<style lang="scss" scoped>
.hero {
  width: 100vw;
  height: 75vh;
  background-position: center;
  background-image: url("../assets/Smile-dog-snow-winter_1920x1080.jpg");
}

h1 {
  position: relative;
  top: 15rem;
  display: flex;
  text-align: center;
  align-items: center;
  justify-content: center;
  padding-right: 60%;
  padding-left: 10%;
  font-size: 50px;

  @media (max-width: 900px) {
    font-size: 30px;
  }
}
</style>
