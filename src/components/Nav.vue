<script setup>
import { RouterLink} from "vue-router";
</script>

<template>
    <nav class="flex max-w-7xl mx-auto p-5 space-x-20 items-baseline">
      <RouterLink to="/" class="text-lg font-bold">Learning Vue</RouterLink>
      <div class="flex space-x-8 text-slate-900 font-semibold">
        <RouterLink to="/" active-class="font-bold border-b-2">Home</RouterLink>
        <RouterLink to="/about" active-class="font-bold border-b-2">About us</RouterLink>
        <RouterLink to="/contact" active-class="font-bold border-b-2">Contact us</RouterLink>
      </div>
    </nav>
</template>
