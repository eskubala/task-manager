<template>
    <div class="sidebar z-30 bg-purple dark:bg-violet h-full w-1/6" :class="{ active: isSidebarActive }">
      <button @click="toggleSidebar" class="absolute right-0">
        <svg class="fill-white dark:fill-light-gray h-[25px]" xmlns="http://www.w3.org/2000/svg" height="1em" viewBox="0 0 448 512"><!--! Font Awesome Free 6.4.2 by @fontawesome - https://fontawesome.com License - https://fontawesome.com/license (Commercial License) Copyright 2023 Fonticons, Inc. --><path d="M0 96C0 78.3 14.3 64 32 64H416c17.7 0 32 14.3 32 32s-14.3 32-32 32H32C14.3 128 0 113.7 0 96zM0 256c0-17.7 14.3-32 32-32H416c17.7 0 32 14.3 32 32s-14.3 32-32 32H32c-17.7 0-32-14.3-32-32zM448 416c0 17.7-14.3 32-32 32H32c-17.7 0-32-14.3-32-32s14.3-32 32-32H416c17.7 0 32 14.3 32 32z"/></svg></button>
    </div>  
</template>


<style scoped>
.sidebar {
  width: 4rem;
  color: white;
  overflow-x: hidden;
  position: fixed;
  top: 0;
  left: 0;
  height: 100%;
  transition: all 0.3s ease;
  }

.sidebar.active {
  width: 20rem;
  left: 0;

}

button {

  color: white;
  border: black;
  padding: 10px 20px;
  cursor: pointer;
}

button:focus {
  outline: none;
}
</style>

<script setup lang="ts">
import {ref} from 'vue'
const isSidebarActive = ref(false)
function toggleSidebar() {
  isSidebarActive.value = !isSidebarActive.value
}

</script>
