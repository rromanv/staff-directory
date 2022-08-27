<script setup>
import MagnifyGlass from './MagnifyGlass.vue'
</script>

<template>
  <div class="wrapper">
    <input
      type="text"
      placeholder="Search Staff Member"
      class="px-3 py-4 placeholder-slate-300 text-slate-600 relative rounded-xl border-0 shadow outline-none focus:outline-none focus:ring focus:ring-slate-500 w-full pl-8"
    />
    <span class="z-10 h-full absolute text-slate-300 text-lg right-0 pr-8 py-4">
      <MagnifyGlass />
    </span>
  </div>
</template>

<style lang="postcss">
.wrapper {
  @apply relative flex w-full flex-wrap items-stretch;
}
</style>
