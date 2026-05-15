<script setup>
const emptyCards = Array.from({ length: 7 });
</script>

<template>
  <div class="w-full flex flex-col gap-5">
    <h2 class="text-preset-5 font-semibold text-neutral-0">
      Daily forecast forecast
    </h2>
    <div class="grid grid-cols-3 md:grid-cols-7 gap-4">
      <div
        v-for="(_, index) in emptyCards"
        :key="index"
        class="w-full h-41.25 bg-neutral-800 border border-neutral-600 rounded-xl"
      ></div>
    </div>
  </div>
</template>
