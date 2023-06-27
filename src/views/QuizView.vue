<script setup>
import quizes from "@/data/quizes.json"
import {useRoute} from "vue-router";
import Question from "@/components/Question.vue";
import QuizHeader from "@/components/QuizHeader.vue";
import {computed, ref} from "vue";

const route = useRoute();

const quizId = parseInt(route.params.id);
const quiz = quizes.find(quiz => quiz.id === quizId);
const currentQuestionIndex = ref(0);

const questionStatus = computed(() => `${currentQuestionIndex.value}/${quiz.questions.length}`);
const barPercentage = computed(() => `${currentQuestionIndex.value/quiz.questions.length * 100}%`)
</script>

<template>
 <div class="mt-5">
    <QuizHeader :questionStatus="questionStatus" :barPercentage="barPercentage" />
    <Question :question="quiz.questions[currentQuestionIndex]" />
   <button class="p-2 bg-gradient-to-r from-blue-500 shadow-sm rounded" @click="currentQuestionIndex++">Next Question</button>
 </div>
</template>

<style scoped>

</style>