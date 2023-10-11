<template>
<div>
    <button @click="toggleTheme" class="bg-white dark:bg-gray shadow-lg dark:shadow-lg z-30 rounded-full">
        <svg class="fill-graphite dark:fill-light-gray" xmlns="http://www.w3.org/2000/svg" height="1em" viewBox="0 0 512 512"><path d="M448 256c0-106-86-192-192-192V448c106 0 192-86 192-192zM0 256a256 256 0 1 1 512 0A256 256 0 1 1 0 256z"/></svg>
    </button>
</div>
</template>
<style scoped>


button {
  cursor: pointer;
  position: fixed;
  bottom: 25px;
  right: 25px;
  width: 40px;
  height: 40px;

}
svg {
    width: 25px;
    height: 25px;
    display: inline-block;
}


button:focus {
  outline: none;
}
</style>

<script setup lang="ts">
import { ref, inject, computed} from 'vue';
//import type { InjectionKey } from 'vue';
const isDarkMode = inject<boolean>('isDarkMode');

  const toggleTheme = () => {
    if (isDarkMode) {
      isDarkMode.value = !isDarkMode.value
    };
  };

  //  const themeClass = computed(() => {
  //    return isDarkMode.value ? 'dark' : '';
  //   });

</script>
