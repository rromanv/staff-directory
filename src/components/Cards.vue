<script setup>
import Card from './Card.vue'
</script>

<template>
  <div class="cards">
    <Card v-for="n in 20" />
  </div>
</template>

<style lang="postcss" scoped>
.cards {
  @apply grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 xl:grid-cols-4 gap-4 container mx-auto mt-8 my-4;
}
</style>
