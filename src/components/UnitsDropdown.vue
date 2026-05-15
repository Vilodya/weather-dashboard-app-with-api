<script setup>
const isOpen = defineModel("open");
</script>

<template>
  <div
    v-if="isOpen"
    class="absolute right-0 top-[calc(100%+10px)] w-53.5 h-103 rounded-xl bg-neutral-800 border border-neutral-600 px-1.75 py-1.25"
  ></div>
</template>
