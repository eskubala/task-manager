<template>
  <SectionHeader title="New Task"/>
   
    <div class="z-30 flex justify-center mr-[30px]">
      <FunctionButton class="bg-orange-light-theme text-white text-xs dark:bg-orange w-[80px] h-[25px] rounded-xs shadow-lg" name="Add" />
      <FunctionButton class=" border border-orange-light-theme text-orange-light-theme text-xs dark:bg-orange w-[80px] h-[25px] rounded-xs shadow-lg" name="Cancel" />
    </div> 
    <div>
      <TimeDropdown />
    </div>
</template>

<script setup lang="ts">
import FunctionButton from './FunctionButton.vue';
import SectionHeader from './SectionHeader.vue';
import TimeDropdown from './TimeDropdown.vue';
defineProps({
  title: String,
  toDoCounter: String,
  doneCounter: String,
})
</script>