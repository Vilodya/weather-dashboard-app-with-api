<script setup>
import Header from "@/components/Header.vue";
import WeatherDashboard from "@/components/WeatherDashboard.vue";
</script>

<template>
  <section class="flex flex-col gap-12 lg:gap-16 min-h-screen">
    <Header />
    <h1>How’s the sky looking today?</h1>
    <WeatherDashboard />
  </section>
</template>
