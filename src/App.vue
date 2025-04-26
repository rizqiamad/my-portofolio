<script setup lang="ts">
import Navbar from "./components/Navbar.vue";
import Footer from "./components/Footer.vue";
</script>

<template>
  <Navbar />
  <div class="max-w-[1200px] mx-auto">
    <RouterView />
  </div>
  <Footer />
</template>
