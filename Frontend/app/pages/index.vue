<template>
  <div class="parent">
    <section class="hero">
      <h1>Get Local & Professional Pet Care with Winterized Yourgi</h1>
    </section>

    <section class="content">
      <img src="../assets/winter-dog-9rej40jms41naniq-1511055065.jpg" />
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

    <section class="content">
      <img src="../assets/1992312-3631488892.jpg" />
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
      <button>Book Now</button>
    </section>

    <section class="content">
      <h2>Thousands of Satisfied Pet Parents</h2>
      <p>
        Our customers love the convenience and care they receive from our
        multiple locations!
      </p>
      <ReviewCarousel />
    </section>

    <section class="content">
      <img src="../assets/wp5326819-2955218145.jpg" />
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
      <button>Book Now</button>
    </section>
    <hr />
    <section class="content">
      <h2>Find a Yourgi Location Near You</h2>
      <div class="location-list">
        <a
          v-for="loc in locations"
          :key="loc"
          :href="`/locations/${loc.toLowerCase().replace(/\\s+/g, '-')}`"
          class="location"
        >
          <span>{{ loc }}</span>
        </a>
      </div>
    </section>
  </div>
</template>

<script setup>
import Snowflake from "~/assets/snowflake.vue";
const locations = [
  "California",
  "Colorado",
  "Connecticut",
  "Florida",
  "Georgia",
  "Idaho",
  "Illinois",
  "Indiana",
  "Louisiana",
  "Maryland",
  "Massachusetts",
  "Minnesota",
  "New Jersey",
  "New York",
  "North Carolina",
  "South Carolina",
  "Tennessee",
  "Texas",
  "Washington",
  "Wisconsin",
];
</script>

<style lang="scss" scoped>
.hero {
  width: 100vw;
  height: 75vh;
  background-position: center;
  background-image: url("../assets/Smile-dog-snow-winter_1920x1080.jpg");
  background-repeat: no-repeat;
  background-size: cover;
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

img {
  min-width: 800px;
  height: 300px;
  object-fit: cover;
  border-radius: 25px;
}

section {
  padding-top: 2rem;
}

.content {
  justify-self: center;
  max-width: 1300px;
}

.location-list {
  display: flex;
  flex-wrap: wrap; /* allows wrapping to next line */
  justify-content: center; /* centers items horizontally */
  gap: 1rem; /* space between items */
  padding: 1rem 0;
}

.location {
  flex: 1 1 calc(25% - 1rem); /* 4 columns by default */
  text-align: center;
  background-color: #f2f2f2;
  border-radius: 0.5rem;
  padding: 10px;
  text-decoration: none;
  color: inherit;
}

hr {
  border: 1px solid red;
}
.parent {
  display: grid;
}
</style>
