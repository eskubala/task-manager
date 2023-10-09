<script setup lang="ts">
//import { RouterLink, RouterView } from 'vue-router'
import MainView from './views/MainView.vue';
import {ref, provide} from 'vue';
const isDarkMode = ref(true);
provide('isDarkMode', isDarkMode);

</script>

<template>
  <div class="app h-100" :class="{dark:isDarkMode}">

    <MainView />
  </div>
</template>

<style scoped>
.app{
  display: flex;
  margin: 4rem
  
}
</style>
