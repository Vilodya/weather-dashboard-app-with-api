<script setup>
import { ref } from "vue";
import IconSettings from "@/assets/icons/icon-settings.svg";
import IconChevronDown from "@/assets/icons/icon-chevron-down.svg";
import UnitsDropdown from "@/components/UnitsDropdown.vue";

const isUnitsDropdownOpen = ref(false);

function toggleUnitsDropdown() {
  isUnitsDropdownOpen.value = !isUnitsDropdownOpen.value;
}
</script>

<template>
  <div class="relative flex justify-between items-center">
    <a href="#" class="block w-34 md:w-49">
      <img class="max-w-full" src="/images/Logo.svg" alt="Weather Now" />
    </a>
    <button
      type="button"
      class="px-2.5 py-2 gap-1.5 bg-neutral-800 hover:bg-neutral-700 rounded-md md:px-4 md:py-3 md:gap-2.5"
      @click="toggleUnitsDropdown()"
    >
      <img :src="IconSettings" alt="" class="w-3.5 md:w-4" />
      <span class="text-preset-8 md:text-preset-7 text-neutral-0">Units</span>
      <img
        :src="IconChevronDown"
        alt=""
        class="w-2.25 md:w-3 transition-transform duration-200"
        :class="isUnitsDropdownOpen ? 'rotate-180' : 'rotate-0'"
      />
    </button>
    <UnitsDropdown v-model:open="isUnitsDropdownOpen" />
  </div>
</template>
