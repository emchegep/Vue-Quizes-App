<script setup>
  import Card from "@/components/Card.vue";
  import {ref, watch} from "vue";
  import q from "@/data/quizes.json";

  const quizes = ref(q);
  const search = ref("")

  watch(search, ()=>{
    quizes.value = q.filter(quiz => quiz.name.toLowerCase().includes(search.value.toLowerCase()))
  })
</script>

<template>
  <div class="mt-2.5 mb-2.5">
    <h1 class="font-bold mr-7">Quizes</h1>
    <input type="text" class="border-0 bg-gray-200 p-2.5 rounded" placeholder="Search..." v-model="search">
  </div>
  <div class="flex flex-wrap mt-8">
    <Card v-for="quiz in quizes" :key="quiz.id" :quiz="quiz" class="motion-safe:hover:scale-[1.01] transition-all"/>
  </div>
  <div>

  </div>
</template>

<style scoped>

</style>