<template>
  <section class="hero">
    <h1>Get Local & Professional Pet Care with Winterized Yourgi</h1>
  </section>

  <section>
    <div>
      <img src="../assets/OIP-389337386.jpg" />
    </div>
    <h2>Discover the Benefits of Trusted Pet Care with Yourgi</h2>
    <div class="icon-list">
      <IconSection
        :icon="Snowflake"
        title="Background-checked Caregivers"
        desc="Yourgi connects you with verified professionals for worry-free pet care."
      />
      <IconSection
        :icon="Snowflake"
        title="We’re Here 24/7"
        desc="Book services anytime, anywhere, and keep your pet happy and healthy."
      />
      <IconSection
        :icon="Snowflake"
        title="Our Trusted Network of Locations"
        desc="Rest easy knowing your pet is in safe hands with our experts."
      />
    </div>
  </section>

  <section>
    <div>
      <img src="../assets/OIP-389337386.jpg" />
    </div>
    <h2>Discover the Benefits of Trusted Pet Care with Yourgi</h2>
    <div class="icon-list">
      <IconSection
        :icon="Snowflake"
        title="Verified professionals for your peace of mind"
      />
      <IconSection
        :icon="Snowflake"
        title="Simple booking at your fingertips"
      />
      <IconSection
        :icon="Snowflake"
        title="Earn rewards while caring for your pets"
      />
    </div>
  </section>
</template>

<script setup>
import Snowflake from "~/assets/snowflake.vue";
</script>

<style lang="scss" scoped>
.hero {
  width: 100vw;
  height: 75vh;
  background-position: center;
  background-image: url("../assets/Smile-dog-snow-winter_1920x1080.jpg");
}

h1 {
  position: relative;
  top: 10rem;
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

section {
  padding-top: 5rem;
}

.icon-list {
  padding-bottom: 50px;
}
</style>
