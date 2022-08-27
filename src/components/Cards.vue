<script setup>
import Search from './Search.vue'
import Card from './Card.vue'
import Pagination from './Pagination.vue'
</script>

<template>
  <div class="wrapper">
    <Search />
    <div class="cards">
      <Card v-for="n in 20" />
    </div>
    <Pagination />
  </div>
</template>

<style lang="postcss" scoped>
.wrapper {
  @apply container mx-auto py-4 flex flex-col gap-4;
  .cards {
    @apply grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 xl:grid-cols-4 gap-4;
  }
}
</style>
