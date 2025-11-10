<template>
  <div class="parent">
    <section class="hero">
      <h1>Get Local & Professional Pet Care with Winterized Yourgi</h1>
    </section>

    <section class="container content">
      <div>
        <img class="content-img" src="../assets/1992312-3631488892.jpg" />
      </div>
      <div>
        <h2>Discover the Benefits of Trusted Pet Care with Yourgi</h2>
        <div>
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
      </div>
    </section>

    <section class="container">
      <div class="content flip">
        <div>
          <h2>Why Rebuild this site with a winter theme?</h2>
          <div>
            <IconSection
              :icon="Snowflake"
              title="Background-checked Caregivers"
            />
            <IconSection :icon="Snowflake" title="We’re Here 24/7" />
            <IconSection
              :icon="Snowflake"
              title="Our Trusted Network of Locations"
            />
          </div>
        </div>
        <div>
          <img
            class="content-img"
            src="../assets/winter-dog-9rej40jms41naniq-1511055065.jpg"
          />
        </div>
      </div>
      <div>
        <button>Book Now</button>
      </div>
    </section>

    <section class="container">
      <h2>Thousands of Satisfied Pet Parents</h2>
      <p>
        Our customers love the convenience and care they receive from our
        multiple locations!
      </p>
      <ReviewCarousel />
    </section>

    <section class="container">
      <div class="content">
        <div>
          <img class="content-img" src="../assets/wp5326819-2955218145.jpg" />
        </div>
        <div>
          <h2>Why Rebuild this site with a winter theme?</h2>
          <div>
            <IconSection
              :icon="Snowflake"
              title="Background-checked Caregivers"
            />
            <IconSection :icon="Snowflake" title="We’re Here 24/7" />
            <IconSection
              :icon="Snowflake"
              title="Our Trusted Network of Locations"
            />
          </div>
        </div>
      </div>
      <div>
        <button>Book Now</button>
      </div>
    </section>

    <hr />
    <section class="container">
      <h2>Find a Festive Yourgi Location Near You</h2>
      <div class="location-list">
        <a v-for="loc in locations" :key="loc" :href="`/`" class="location">
          <span>{{ loc }}</span>
        </a>
      </div>
    </section>
  </div>
</template>

<script setup>
import Snowflake from "~/assets/snowflake.vue";
const locations = [
  "Gumdrop Forest",
  "Candy Cane Lane",
  "The North Pole",
  "Marshmallow Mountain",
  "Sugarplum Square",
  "Peppermint Plaza",
  "Snowball Park",
  "Winter Wonderland",
  "Cocoa Campground",
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

  @media (max-width: 1000px) {
    font-size: 30px;
  }
}

h2 {
  font-size: 50px;
  margin-top: 30px;
}

section {
  padding-top: 2rem;
}

.content-img {
  width: 100%;
  min-height: 100%;
  max-width: 800px;
  border-radius: 25px;
  object-fit: cover;
}

.content {
  display: flex;
  align-items: stretch;
  gap: 60px;

  @media (max-width: 1000px) {
    flex-direction: column;
    align-items: center;
  }
}

.container {
  padding-left: 40px;
  padding-right: 40px;
  justify-content: center;
  max-width: 1300px;
  margin: 0 auto;
}

.location-list {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  gap: 1rem;
  padding: 1rem 0;
}

.location {
  flex: 1 1 calc(25% - 1rem);
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

.flip {
  @media (max-width: 1000px) {
    flex-direction: column-reverse;
  }
}
</style>
