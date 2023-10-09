<template>
    <div class="sidebar z-30 bg-violet h-full w-1/6" :class="{ active: isSidebarActive }">
      <button @click="toggleSidebar">Toggle Sidebar</button>
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
