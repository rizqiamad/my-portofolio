<script setup lang="ts">
import { MotionComponent, MotionGroupComponent } from "@vueuse/motion";
import Backend from "../components/Backend.vue";
import DbTools from "../components/DbTools.vue";
import Frontend from "../components/Frontend.vue";

const initial = {
  opacity: 0,
  y: 100,
};

const enter = {
  opacity: 1,
  y: 0,
  transition: {
    duration: 800,
  },
};
</script>

<template>
  <div class="px-4">
    <div class="text-center pt-28 pb-20">
      <h1
        class="text-xl xxs:text-2xl xs:text-4xl sm:text-5xl md:text-6xl font-bold"
        v-motion
        :initial="initial"
        :enter="enter"
      >
        Fullstack Developer
      </h1>
      <h1
        class="text-xl xxs:text-2xl xs:text-4xl sm:text-5xl md:text-6xl font-bold"
        v-motion
        :initial="initial"
        :enter="enter"
      >
        Keeping growth with tech
      </h1>
      <div class="mt-10 flex gap-4 items-center justify-center overflow-hidden">
        <MotionComponent
          is="a"
          preset="slideVisibleLeft"
          duration="800"
          href="#projects"
          class="text-sm sm:text-base font-semibold py-2 px-4 sm:px-6 bg-blue-500 hover:bg-blue-600 text-white/90 rounded-md cursor-pointer"
        >
          My Project
        </MotionComponent>
        <MotionComponent
          is="a"
          preset="slideVisibleRight"
          duration="800"
          href="#skills"
          class="text-sm sm:text-base font-semibold py-2 px-4 sm:px-8 bg-secondary hover:bg-secondary/80 text-white/90 rounded-md border border-white/20 cursor-pointer"
        >
          My Skills
        </MotionComponent>
      </div>
    </div>
    <div
      style="background-image: url(/src/assets/dicoding-event.jpg)"
      class="aspect-[12/9] bg-cover rounded-2xl bg-center mb-10"
    />
    <MotionGroupComponent
      is="div"
      preset="slideVisibleLeft"
      :duration="600"
      id="skills"
      class="flex gap-10 flex-col lg:flex-row scroll-mt-20"
    >
      <Frontend />
      <Backend />
      <DbTools />
    </MotionGroupComponent>
    <section id="projects-container">
      <div id="projects" class="mt-10 scroll-mt-20 sm:scroll-mt-0">
        <div
          class="flex gap-4 flex-col sm:flex-row h-[25rem] lg:h-[40rem] items-center mb-10"
          v-motion-pop-visible
        >
          <div class="sm:flex-1">
            <h2 class="font-semibold text-xl sm:text-2xl mb-4">
              Job Board App
            </h2>
            <p class="sm:text-base text-sm">
              Talent Bridge is a job board web app getting role as an aggregator
              which is bringing togather jobseeker and employer. This platform
              assists jobseekers to find out their dream job, meanwhile company
              can recruite their demanded employee for their demanded role.
            </p>
            <p class="mt-4">
              <a
                class="py-2 px-4 font-semibold hover:bg-yellow-400 bg-yellow-300 rounded-lg text-black"
                target="_blank"
                href="https://talentsbridge.vercel.app/"
                >Visit Link</a
              >
            </p>
          </div>
          <div
            style="background-image: url(/src/assets/portofolio/finpro.png)"
            class="sm:flex-1/6 sm:aspect-[12/9] bg-cover bg-center rounded-2xl h-full w-full"
          />
        </div>
        <div
          class="flex gap-4 flex-col sm:flex-row h-[25rem] lg:h-[40rem] items-center mb-10"
          v-motion-pop-visible
        >
          <div class="sm:flex-1">
            <h2 class="font-semibold text-xl sm:text-2xl mb-4">
              Event Ticketing App
            </h2>
            <p class="sm:text-base text-sm">
              Web Event Ticketing App is an aggregator app inspired by
              <a
                href="https://loket.com/"
                target="_blank"
                class="border-b border-dashed hover:text-blue-500 hover:border-blue-500"
                >Loket</a
              >. People are able to visit this web app and signing up themself
              either as customer or organizer who create event. Customer can buy
              the event tickets and make a transaction inside the web app, also
              customer who attanded the event can give rating for the organizer.
            </p>
            <p class="mt-4">
              <a
                class="py-2 px-4 font-semibold hover:bg-yellow-400 bg-yellow-300 rounded-lg text-black"
                target="_blank"
                href="https://minpro-frontend.vercel.app/"
                >Visit Link</a
              >
            </p>
          </div>
          <div
            style="background-image: url(/src/assets/portofolio/minpro.png)"
            class="sm:flex-1/6 sm:aspect-[12/9] bg-cover bg-center rounded-2xl h-full w-full"
          />
        </div>
        <div
          class="flex gap-4 flex-col sm:flex-row h-[25rem] lg:h-[40rem] items-center mb-10"
          v-motion-pop-visible
        >
          <div class="sm:flex-1">
            <h2 class="font-semibold text-xl sm:text-2xl mb-4">
              Asus ROG Company Profile
            </h2>
            <p class="sm:text-base text-sm">
              Website company profile inspired by rog asus official website
              <a
                href="https://rog.asus.com/"
                target="_blank"
                class="border-b border-dashed hover:text-blue-500 hover:border-blue-500"
                >Asus</a
              >. Featuring a dark theme with neon accents and dynamic
              animations, it creates a visually striking experience while
              showcasing the company&apos;s identity, products, and teams.
            </p>
            <p class="mt-4">
              <a
                class="py-2 px-4 font-semibold hover:bg-yellow-400 bg-yellow-300 rounded-lg text-black"
                target="_blank"
                href="https://rog-company-profile.vercel.app/"
                >Visit Link</a
              >
            </p>
          </div>
          <div
            style="
              background-image: url(/src/assets/portofolio/company-profile.png);
            "
            class="sm:flex-1/6 sm:aspect-[12/9] bg-cover bg-center rounded-2xl h-full w-full"
          />
        </div>
      </div>
    </section>
  </div>
</template>

<style>
.animation {
  transform: translateY(40px);
  opacity: 0;
}
</style>
