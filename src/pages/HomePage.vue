<script setup>
import Header from "@/components/Header.vue";
import WeatherDashboard from "@/components/WeatherDashboard.vue";
</script>

<template>
  <section
    class="w-full min-h-screen pt-4 md:pt-6 lg:pt-12 pb-12 md:pb-20 bg-neutral-900"
  >
    <div class="mx-auto max-w-360 px-4 md:px-6 lg:px-28">
      <div class="flex flex-col gap-12 lg:gap-16">
        <Header />
        <h1 class="text-preset-2 text-neutral-0 text-center">
          How’s the sky looking today?
        </h1>
        <WeatherDashboard />
      </div>
    </div>
  </section>
</template>
