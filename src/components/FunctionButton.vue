<template>
    <button>{{ name }}</button> 
</template>

<script setup lang="ts">
defineProps({
  name: String,
})
</script>