<script setup lang="ts">
import SidebarApp from '../components/SidebarApp.vue';
import DarkModeButton from '@/components/DarkModeButton.vue';
import SectionHeader from '@/components/SectionHeader.vue';
import TaskCounter from '@/components/TaskCounter.vue';
import AddTaskComponent from '@/components/AddTaskComponent.vue';
</script>
<template>
  <SidebarApp />
  <div class="relative flex justify-center min-w-full h-[100%] bg-mud-white dark:bg-dark-gray">
      <div class="absolute flex  z-10 p-8 m-14 h-[90%] w-[90%] bg-white dark:bg-gray shadow-lg dark:shadow-lg rounded-lg">
        <div class="w-1/4">
          <SectionHeader title="Tasks"/>
          <div class="flex flex-row justify-between">
            <TaskCounter class="bg-yellow opacity-[65%] dark:bg-limon text-dark-gray" title="To do" to-do-counter="3" />
            <TaskCounter class="bg-green-light-theme opacity-[65%] dark:bg-limon m-auto" title="Done" to-do-counter="3" />
          </div>
          <div>
            <AddTaskComponent />
          </div>
        </div>
        <div class="w-2/4">
          <SectionHeader title="Project 1's Schedule"/>
        </div>
        <div class="w-1/4">
          <SectionHeader title="Progress"/>
        </div>
      </div>
      <div class="absolute z-20 h-[100%] w-[100%] max-w-[43%] pt-0 mt-0 bg-violet opacity-10">
          <!-- Your content -->
      </div>
  </div>
  <DarkModeButton />
</template>
