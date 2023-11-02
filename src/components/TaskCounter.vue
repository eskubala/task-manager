<template>
      <div class="z-30 w-1/2 h-[125px] flex flex-col rounded-md text-center mr-[30px]">
        <span class="text-dark-gray dark:text-light-gray text-xl">{{toDoCounter}}</span>
        <span class="text-dark-gray dark:text-light-gray text-sm mt-[-20px]">{{title}}</span>      
      </div> 
</template>

<script setup lang="ts">
defineProps({
    title: String,
    toDoCounter: String,
    doneCounter: String,
})
</script>