<template>

<div>
    <button class="inline-flex px-3 py-2 text-xs" @click="toggleDropdown">Daily
      <svg class="-mr-1 h-5 w-5 text-gray-400 flex justify-end" viewBox="0 0 20 20" fill="currentColor" aria-hidden="true">
        <path fill-rule="evenodd" d="M5.23 7.21a.75.75 0 011.06.02L10 11.168l3.71-3.938a.75.75 0 111.08 1.04l-4.25 4.5a.75.75 0 01-1.08 0l-4.25-4.5a.75.75 0 01.02-1.06z" clip-rule="evenodd" />
      </svg>
    </button>
    <div v-if="isDropdownOpen" class="dropdown">
      <div class="py-1" role="none">
        <a href="#" class="text-gray-700 block px-4 py-2 text-xs" role="menuitem" tabindex="-1" id="menu-item-0">Daily</a>
        <a href="#" class="text-gray-700 block px-4 py-2 text-xs" role="menuitem" tabindex="-1" id="menu-item-1">Weekly</a>
        <a href="#" class="text-gray-700 block px-4 py-2 text-xs" role="menuitem" tabindex="-1" id="menu-item-2">Monthly</a>
      </div>
    </div>
  </div>
</template>

<script setup lang="ts">
import { ref } from 'vue';
    const isDropdownOpen = ref(false);

    const toggleDropdown = () => {
      isDropdownOpen.value = !isDropdownOpen.value;
    };
</script>