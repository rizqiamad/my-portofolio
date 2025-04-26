<script setup lang="ts">
import { MotionComponent, MotionGroupComponent } from "@vueuse/motion";
</script>

<template>
  <div class="px-4">
    <div class="animated-bg"></div>
    <section
      class="flex-col md:flex-row relative flex items-center justify-center py-20 text-white overflow-hidden gap-5 sm:gap-20"
    >
      <MotionComponent
        is="div"
        preset="slideVisibleLeft"
        duration="800"
        class="rounded-t-full bg-linear-to-r from-primary to-[#0432bb4d]/30 flex-1 h-[30rem] flex justify-center"
      >
        <img src="/src/assets/hanifahmad.png" alt="Hanif Ahmad Rizqullah" />
      </MotionComponent>

      <MotionGroupComponent
        is="div"
        preset="slideVisibleRight"
        duration="800"
        class="flex-1"
      >
        <h1 class="text-xl xxs:text-2xl xs:text-4xl font-semibold mb-10">
          Hanif Ahmad Rizqullah
        </h1>
        <p class="sm:text-base text-sm">
          My name is Hanif Ahmad Rizqullah, a self-taught developer without a
          degree, graduating from senior high school. After resigning from
          college after a year of study, I decided to pursue other opportunities
          available in the world. Eventually, I chose programming after careful
          consideration. I then joined a bootcamp and completed a full-stack web
          development program. Being exposed to various technologies has
          increased my curiosity about the tech world, and I am committed to
          pursuing this career for the long term.
        </p>
      </MotionGroupComponent>
    </section>
  </div>
</template>

<style scoped>
.animated-bg {
  position: fixed;
  top: 0;
  left: 0;
  width: 100vw;
  height: 100vh;
  background: radial-gradient(
    circle at 50% 50%,
    rgba(50, 100, 255, 0.3) 10%,
    transparent 70%
  );
  animation: pulseGlow 3s infinite alternate;
}

@keyframes pulseGlow {
  0% {
    transform: scale(1);
    opacity: 0.3;
    filter: blur(20px);
  }
  50% {
    transform: scale(1.2);
    opacity: 0.5;
    filter: blur(30px);
  }
  100% {
    transform: scale(1);
    opacity: 0.3;
    filter: blur(20px);
  }
}
</style>
