<template>
    <div class="z-30 ">
      <p class="text-dark-gray dark:text-light-gray text-base">{{title}}</p>
    </div>  
</template>

<script setup lang="ts">
defineProps({
    title: String
})
</script>