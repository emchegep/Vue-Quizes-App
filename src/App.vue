<script setup>
  import {RouterView } from "vue-router"
  import Nav from "@/components/Nav.vue";

</script>

<template>
  <div>
    <header class="bg-gradient-to-r from-blue-500 shadow-sm">
      <Nav />
    </header>
    <main class="max-w-7xl mx-auto p-5">
      <RouterView />
    </main>
  </div>
</template>

