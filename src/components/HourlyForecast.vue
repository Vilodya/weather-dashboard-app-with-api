<script setup>
import { ref } from "vue";
import IconChevronDown from "@/assets/icons/icon-chevron-down.svg";
import DaysDropdown from "@/components/DaysDropdown.vue";

const isDaysDropdownOpen = ref(false);
const selectedDay = ref("-");

function toggleDaysDropdown() {
  isDaysDropdownOpen.value = !isDaysDropdownOpen.value;
}

function handleSelectDay(day) {
  selectedDay.value = day;
}

const emptyCards = Array.from({ length: 8 });
</script>

<template>
  <div class="w-full px-4 py-5 md:px-6 md:py-6 rounded-[20px] bg-neutral-800">
    <div class="relative flex items-center justify-between w-full gap-4">
      <h2 class="text-preset-5 font-semibold text-neutral-0">
        Hourly forecast
      </h2>
      <button
        type="button"
        class="px-4 py-2.25 gap-3 bg-neutral-600 hover:bg-neutral-300 rounded-lg"
        @click="toggleDaysDropdown()"
      >
        <span class="text-preset-7 text-neutral-0">{{ selectedDay }}</span>
        <img
          :src="IconChevronDown"
          alt=""
          class="w-3 transition-transform duration-200"
          :class="isDaysDropdownOpen ? 'rotate-180' : 'rotate-0'"
        />
      </button>
      <DaysDropdown
        v-model:open="isDaysDropdownOpen"
        @select-day="handleSelectDay"
      />
    </div>
    <div class="mt-4 flex flex-col gap-4 overflow-y-auto h-148">
      <div
        v-for="(_, index) in emptyCards"
        :key="index"
        class="w-full h-15 bg-neutral-700 border border-neutral-600 rounded-lg"
      ></div>
    </div>
  </div>
</template>
