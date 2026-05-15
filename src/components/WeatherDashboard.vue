<script setup>
import Search from "@/components/Search.vue";
import HourlyForecast from "@/components/HourlyForecast.vue";
import DailyForecast from "@/components/DailyForecast.vue";
import CurrentWeatherOverview from "@/components/CurrentWeatherOverview.vue";
</script>

<template>
  <div class="flex flex-col gap-8 lg:gap-12">
    <Search />
    <div
      class="grid grid-cols-1 gap-8 lg:grid-cols-[minmax(680px,1fr)_minmax(250px,384px)]"
    >
      <div
        class="w-full flex flex-col gap-8 lg:flex-1 lg:gap-12 justify-between"
      >
        <CurrentWeatherOverview />
        <DailyForecast />
      </div>
      <HourlyForecast />
    </div>
  </div>
</template>
