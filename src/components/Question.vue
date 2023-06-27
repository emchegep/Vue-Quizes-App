<script setup>
const { question } = defineProps(['question']);


</script>

<template>
  <div class="mt-5">
    <div class="mb-5">
      <h2 class="text-4xl">
        {{  question.text }}
      </h2>
    </div>
    <div>
      <div class="flex mb-5 cursor-pointer" v-for="option in question.options" :key="option.id">
        <p class="flex items-center justify-center bg-amber-400 w-12 h-12 text-3xl">{{  option.label }}</p>
        <div class="flex items-center w-full text-3xl py-0 px-5 bg-gray-200">
          <p>{{  option.text }}</p>
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>

</style>