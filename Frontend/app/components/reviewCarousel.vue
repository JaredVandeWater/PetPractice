<script setup>
import "vue3-carousel/carousel.css";
import { Carousel, Slide, Navigation, Pagination } from "vue3-carousel";

const config = {
  height: 250,
  itemsToShow: 3, // default for large screens
  gap: 20,
  wrapAround: true,
  breakpoints: {
    1200: {
      // >= 1200px
      itemsToShow: 3,
    },
    900: {
      // >= 900px
      itemsToShow: 2,
    },
    600: {
      // >= 600px
      itemsToShow: 1,
    },
  },
};

const reviews = [
  {
    id: 1,
    text: "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Praesent...",
    author: "Alice",
    location: "New York",
  },
  {
    id: 2,
    text: "Sed do eiusmod tempor incididunt ut labore et dolore magna aliqua...",
    author: "Bob",
    location: "Los Angeles",
  },
  {
    id: 3,
    text: "Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris...",
    author: "Charlie",
    location: "Chicago",
  },
  {
    id: 4,
    text: "Duis aute irure dolor in reprehenderit in voluptate velit esse...",
    author: "Diana",
    location: "Miami",
  },
  {
    id: 5,
    text: "Excepteur sint occaecat cupidatat non proident, sunt in culpa...",
    author: "Eve",
    location: "Seattle",
  },
];
</script>

<template>
  <Carousel v-bind="config">
    <Slide v-for="review in reviews" :key="review.id">
      <div class="review-card">
        <p class="text">“{{ review.text }}”</p>
        <p class="author">— {{ review.author }}, {{ review.location }}</p>
      </div>
    </Slide>

    <template #addons>
      <Navigation />
      <Pagination class="pagination" />
    </template>
  </Carousel>
</template>

<style scoped lang="scss">
.review-card {
  background-color: #f8f8f8;
  padding: 1rem;
  border-radius: 8px;
  height: 100%; // ensures cards fill carousel height
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  padding-bottom: 100px;

  .text {
    font-size: 1rem;
    margin-bottom: 0.5rem;
  }

  .author {
    font-weight: 600;
    font-size: 0.9rem;
    color: #555;
  }
}

/* Optional: customize carousel navigation buttons */
.carousel {
  --vc-nav-background: rgba(0, 0, 0, 0.7);
  --vc-nav-border-radius: 100%;
  --vc-nav-size: 2rem;
}

.pagination {
  top: 280px;
}
</style>
