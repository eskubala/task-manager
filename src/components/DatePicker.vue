<template>
    <div>
      <input type="text" v-model="selectedDate" @click="openDatePicker" />
      <div v-if="isDatePickerOpen" class="date-picker">
        <div class="calendar-header">
          <button @click="previousMonth">&lt;</button>
          {{ currentMonth }}
          <button @click="nextMonth">&gt;</button>
        </div>
        <div class="calendar">
          <div class="day" v-for="day in daysInMonth" :key="day">
            {{ day }}
          </div>
        </div>
      </div>
    </div>
  </template>
  
  <script setup lang="ts">
  import { ref, computed } from 'vue';
  import { format, addMonths, subMonths, startOfMonth, endOfMonth, eachDayOfInterval } from 'date-fns';
  
      const selectedDate = ref('');
      const isDatePickerOpen = ref(false);
      const currentDate = ref(new Date());
  
      const currentMonth = computed(() => format(currentDate.value, 'MMMM yyyy'));
      const daysInMonth = computed(() => {
        const start = startOfMonth(currentDate.value);
        const end = endOfMonth(currentDate.value);
        return eachDayOfInterval({ start, end });
      });
  
      const openDatePicker = () => {
        isDatePickerOpen.value = !isDatePickerOpen.value;
      };
  
      const previousMonth = () => {
        currentDate.value = subMonths(currentDate.value, 1);
      };
  
      const nextMonth = () => {
        currentDate.value = addMonths(currentDate.value, 1);
      };
  

  </script>
  
  <style scoped>
  .date-picker {
    position: absolute;
    background: white;
    border: 1px solid #ccc;
    padding: 10px;
    top: 40px;
    left: 0;
  }
  
  .calendar-header {
    display: flex;
    justify-content: space-between;
  }
  
  .day {
    display: inline-block;
    width: 30px;
    height: 30px;
    line-height: 30px;
    text-align: center;
    border: 1px solid #ccc;
    margin: 2px;
  }
  </style>
  