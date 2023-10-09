<script setup lang="ts">
import SidebarApp from '../components/SidebarApp.vue';
import DarkModeButton from '@/components/DarkModeButton.vue';
</script>
<template>
  <SidebarApp />
  <div class="relative flex justify-center min-w-full h-[100%] bg-dark-gray dark:bg-white">
      <div class="absolute z-10 p-8 m-14 h-[90%] w-[90%] bg-gray dark:bg-white rounded-[35px]">
        <!-- Your content -->
      </div>
      <div class="absolute z-20 h-[100%] w-[100%] max-w-[50%] pt-0 mt-0 bg-violet opacity-10">
          <!-- Your content -->
      </div>
  </div>
  <DarkModeButton />
</template>
