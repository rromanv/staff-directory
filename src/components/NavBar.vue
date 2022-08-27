<script setup>
import { ref } from 'vue'
const title = ref('Staff Directory 👍')
</script>

<template>
  <nav>
    <div class="wrapper">
      <div class="brand">
        <span class="text-2xl font-thin">{{ title }}</span>
      </div>
      <div class="menu">
        <a href="#" class="menu-item">Departments</a>
        <a href="#" class="menu-item">Settings</a>
        <a href="#" class="logout">Logout</a>
      </div>
    </div>
  </nav>
</template>

<style scoped lang="postcss">
nav {
  @apply bg-slate-900 text-slate-200 flex justify-between items-center h-20;
  .wrapper {
    @apply flex justify-between items-center w-full max-w-7xl mx-auto;
    .brand {
      @apply flex items-center;
    }
    .menu {
      @apply flex gap-2;
      .menu-item {
        @apply px-4 py-2 rounded-md hover:bg-gray-200 hover:text-slate-900;
      }
      .logout {
        @apply px-4 py-2 rounded-md hover:bg-gray-200 bg-red-500 hover:text-red-500;
      }
    }
  }
}
</style>
