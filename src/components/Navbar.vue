<script lang="ts" setup>
import { onMounted, onUnmounted, ref } from "vue";
import { RouterLink } from "vue-router";

const scrollVertical = ref(scrollY);
const isOpen = ref(false);

const handleScroll = () => {
  scrollVertical.value = scrollY;
  isOpen.value = false;
};

const handleOpen = () => {
  isOpen.value = !isOpen.value;
};

onMounted(() => {
  window.addEventListener("scroll", handleScroll);
});

onUnmounted(() => {
  window.removeEventListener("scroll", handleScroll);
});
</script>

<template>
  <header
    class="z-50 flex max-w-[1200px] mx-auto items-center py-2 sticky top-4 gap-10 px-4 transition duration-300"
    :class="scrollVertical > 0 && 'bg-primary border rounded-full border-white/20'"
  >
    <RouterLink class="text-white/90 text-base sm:text-xl font-bold" to="/"
      >Hanif Ahmad</RouterLink
    >
    <nav class="hidden sm:flex items-center gap-4 flex-grow-1">
      <RouterLink class="font-semibold text-white/70 hover:text-white" to="/"
        >Home</RouterLink
      >
      <RouterLink
        class="font-semibold text-white/70 hover:text-white"
        to="/about"
        >About</RouterLink
      >
    </nav>
    <a
      class="hidden sm:block text-white/90 font-semibold cursor-pointer hover:bg-blue-600 bg-blue-500 px-4 py-1 rounded-full"
      download="Hanif Ahmad Rizqullah_CV.pdf"
      href="/cv.pdf"
    >
      DOWNLOAD CV
    </a>
    <div class="sm:hidden block relative text-white/90 ml-auto">
      <button class="cursor-pointer" @click="handleOpen">
        <svg
          v-if="!isOpen"
          class="w-4 h-4"
          aria-hidden="true"
          xmlns="http://www.w3.org/2000/svg"
          fill="none"
          viewBox="0 0 17 14"
        >
          <path
            stroke="currentColor"
            stroke-linecap="round"
            stroke-linejoin="round"
            stroke-width="2"
            d="M1 1h15M1 7h15M1 13h15"
          />
        </svg>
        <svg
          v-else
          class="w-4 h-4 text-white/90"
          aria-hidden="true"
          xmlns="http://www.w3.org/2000/svg"
          width="24"
          height="24"
          fill="none"
          viewBox="0 0 24 24"
        >
          <path
            stroke="currentColor"
            stroke-linecap="round"
            stroke-linejoin="round"
            stroke-width="2"
            d="M6 18 17.94 6M18 18 6.06 6"
          />
        </svg>
      </button>
      <div
        v-if="isOpen"
        class="absolute top-5 right-5 flex flex-col border border-white/20 bg-primary w-[10rem] gap-2 p-2 rounded-lg shadow"
      >
        <RouterLink
          to="/"
          class="text-sm font-semibold hover:bg-secondary px-2 py-1 rounded-lg"
          >Home</RouterLink
        >
        <RouterLink
          to="/about"
          class="text-sm font-semibold hover:bg-secondary px-2 py-1 rounded-lg"
          >About</RouterLink
        >
        <a
          class="text-sm text-white/90 font-semibold cursor-pointer hover:bg-blue-600 bg-blue-500 text-center py-1 rounded-full"
          download="Hanif Ahmad Rizqullah_CV.pdf"
          href="/cv.pdf"
        >
          DOWNLOAD CV
        </a>
      </div>
    </div>
  </header>
</template>
