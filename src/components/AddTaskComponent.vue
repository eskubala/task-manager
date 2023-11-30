<template>
  <form class="shadow-lg rounded-md h-1/4 p-4">
    <InputForm class="bg-orange-light-theme text-white text-xs dark:bg-orange rounded-xs justify-center"/>
    <CheckboxForm />
   <div class="z-30 flex justify-center mr-[30px] p-4">
     <FunctionButton class="bg-orange-light-theme text-white text-xs dark:bg-orange w-[80px] h-[25px] rounded-xs shadow-lg" name="Add" />
     <FunctionButton class=" border border-orange-light-theme text-orange-light-theme text-xs dark:bg-orange w-[80px] h-[25px] rounded-xs shadow-lg" name="Cancel" />
   </div> 
   <div class="p-4">
     <TimeDropdown class="bg-pigeon rounded-xs w-full mr-4"/>
   </div>
   
    <InputForm class="bg-pigeon rounded-xs w-full mr-4" />
   
  </form>
 
</template>

<script setup lang="ts">
import FunctionButton from './FunctionButton.vue';
import TimeDropdown from './TimeDropdown.vue';
import InputForm from './InputForm.vue';
import CheckboxForm from './CheckboxForm.vue';


defineProps({
  title: String,
  toDoCounter: String,
  doneCounter: String,
})
</script>