<script setup>
import { useRouter} from "vue-router";

const { quiz } = defineProps(['quiz'])

const router = useRouter()

const navigateToQuiz = () => {
  router.push(`/quiz/${quiz.id}`)
}
</script>

<template>
  <div @click="navigateToQuiz" class="w-80 overflow-hidden rounded shadow mb-9 mr-5 cursor-pointer">
    <img :src="quiz.img" class="w-full h-48 m-0">
    <div class="py-0 px-1.5">
      <h2 class="font-bold">{{  quiz.name }}</h2>
      <p>{{ quiz.questions.length }} Questions</p>
    </div>
  </div>
</template>
