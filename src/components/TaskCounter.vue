<template>
      <div class="z-30 w-[125px] h-[125px] rounded-[25px] text-center">
        <p class="text-dark-gray dark:text-light-gray text-xl">{{toDoCounter}}</p>
        <p class="text-dark-gray dark:text-light-gray text-sm">{{title}}</p>
      </div> 
</template>

<script setup lang="ts">
defineProps({
    title: String,
    toDoCounter: String,
    doneCounter: String,
})
</script>