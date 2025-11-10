<template>
  <div class="icon-section" :class="{ 'no-desc': !desc }">
    <component :is="icon" class="icon" />
    <div>
      <h3>{{ title }}</h3>
      <p v-if="desc">{{ desc }}</p>
    </div>
  </div>
</template>

<script setup lang="ts">
const props = defineProps<{
  icon: Component;
  title: string;
  desc?: string;
}>();
</script>

<style lang="scss" scoped>
.icon-section {
  display: flex;
  align-items: center;
  gap: 25px;
  padding-bottom: 50px;

  .icon {
    flex-shrink: 0;
    height: 40px;
    width: 40px;
    background-color: rgb(216, 255, 255);
    border-radius: 100%;
    padding: 10px;
  }

  h3 {
    margin: 0;
    margin-bottom: 10px;
    font-size: 25px;
  }

  p {
    margin: 0;
    font-size: 20px;
  }

  &.no-desc {
    h3 {
      margin-bottom: 0;
    }
  }
}
</style>
