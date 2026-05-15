<script setup>
const cards = [
  {
    name: "Feels Like",
    value: "-",
  },
  {
    name: "Humidity",
    value: "-",
  },
  {
    name: "Wind",
    value: "-",
  },
  {
    name: "Precipitation",
    value: "-",
  },
];
</script>

<template>
  <div class="flex flex-col gap-5 lg:gap-8">
    <div class="h-71.5 rounded-[20px] w-full bg-neutral-800"></div>
    <div class="grid grid-cols-2 md:grid-cols-4 gap-5">
      <div
        v-for="card in cards"
        class="w-full h-29.5 bg-neutral-800 border border-neutral-600 rounded-xl p-4.75 flex flex-col justify-between"
      >
        <p class="text-preset-6 text-neutral-200">{{ card.name }}</p>
        <p class="text-preset-3 text-neutral-0">{{ card.value }}</p>
      </div>
    </div>
  </div>
</template>
