<script setup>
const emit = defineEmits(["select-day"]);

const isOpen = defineModel("open");

const buttons = [
  { day: "Monday" },
  { day: "Tuesday" },
  { day: "Wednesday" },
  { day: "Thursday" },
  { day: "Friday" },
  { day: "Saturday" },
  { day: "Sunday" },
];

function handleSelectDay(day) {
  emit("select-day", day);
  isOpen.value = false;
}
</script>

<template>
  <div
    v-if="isOpen"
    class="absolute right-0 top-[calc(100%+10px)] w-53.5 rounded-xl bg-neutral-800 border border-neutral-600 p-1.75"
  >
    <div class="flex flex-col gap-1">
      <button
        v-for="button in buttons"
        :key="button.day"
        type="button"
        class="px-2 py-2.5 gap-1 bg-neutral-800 hover:bg-neutral-700 rounded-lg text-preset-7 text-neutral-0"
        @click="handleSelectDay(button.day)"
      >
        {{ button.day }}
      </button>
    </div>
  </div>
</template>
