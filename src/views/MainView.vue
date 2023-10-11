<script setup lang="ts">
import SidebarApp from '../components/SidebarApp.vue';
import DarkModeButton from '@/components/DarkModeButton.vue';
import SectionHeader from '@/components/SectionHeader.vue';
import TaskCounter from '@/components/TaskCounter.vue';
</script>
<template>
  <SidebarApp />
  <div class="relative flex justify-center min-w-full h-[100%] bg-mud-white dark:bg-dark-gray">
      <div class="absolute flex  z-10 p-8 m-14 h-[90%] w-[90%] bg-white dark:bg-gray shadow-lg dark:shadow-lg rounded-[35px]">
        <div class="w-1/4">
          <SectionHeader title="Tasks"/>
          <div>
            <TaskCounter title="To do" to-do-counter="3" />
          </div>
        </div>
        <div class="w-2/4">
          <SectionHeader title="Project 1's Schedule"/>
        </div>
        <div class="w-1/4">
          <SectionHeader title="Progress"/>
        </div>
      </div>
      <div class="absolute z-20 h-[100%] w-[100%] max-w-[44%] pt-0 mt-0 bg-violet opacity-10">
          <!-- Your content -->
      </div>
  </div>
  <DarkModeButton />
</template>
