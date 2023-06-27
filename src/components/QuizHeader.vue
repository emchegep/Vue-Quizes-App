<script setup>
const {questionStatus, barPercentage} = defineProps(['questionStatus','barPercentage'])
</script>

<template>
  <div>
    <h1 class="text-3xl">Question {{  questionStatus }}</h1>
    <div class="w-72 h-12 border-2 border-amber-400">
      <div class="h-full bg-amber-400" :style="{width: barPercentage }">
      </div>
    </div>
  </div>
</template>
