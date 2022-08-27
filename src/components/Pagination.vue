<script setup>
import { ref } from 'vue'
const pages = ref(10)
const activePage = ref(4)

const prevPage = () => {
  if (activePage.value > 1) {
    activePage.value--
  }
}
const nextPage = () => {
  if (activePage.value < pages.value) {
    activePage.value++
  }
}
</script>

<template>
  <div class="pagination">
    <button class="action" :disabled="activePage === 1" @click="prevPage">
      Prev
    </button>
    <button
      class="page"
      v-for="page in pages"
      :class="page === activePage ? 'active' : ''"
      @click="activePage = page"
    >
      {{ page }}
    </button>
    <button class="action" :disabled="activePage === pages" @click="nextPage">
      Next
    </button>
  </div>
</template>

<style lang="postcss" scoped>
.pagination {
  @apply flex justify-center gap-4;
  .action {
    @apply bg-slate-100 p-2 rounded shadow-md text-slate-700 font-medium disabled:text-slate-400 hover:bg-slate-200 hover:disabled:bg-slate-100;
  }
  .page {
    @apply bg-slate-100 p-2 rounded shadow-md text-slate-700 font-medium hover:bg-slate-200;
    &.active {
      @apply bg-yellow-700 text-white;
    }
  }
}
</style>
