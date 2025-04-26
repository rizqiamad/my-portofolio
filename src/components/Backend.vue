<script lang="ts" setup>
import Golang from "/programming-language/golang.png";
import Nodejs from "/programming-language/nodejs.png";
import Express from "/programming-language/express.png";

const icons = [Golang, Nodejs, Express];
</script>

<template>
  <div
    class="flex-1 lg:min-h-[23em] bg-secondary/20 p-4 rounded-xl border border-white/20"
  >
    <h2 class="font-semibold text-xl sm:text-2xl mb-4">Backend</h2>
    <p class="sm:text-base text-sm">
      Backend side is the backbone of the dynamic web application, so
      that&apos;s why i use
      <a
        href="https://nodejs.org/en"
        target="_blank"
        class="border-b border-dashed hover:text-blue-500 hover:border-blue-500"
        >Nodejs</a
      >
      and
      <a
        href="https://expressjs.com/"
        target="_blank"
        class="border-b border-dashed hover:text-blue-500 hover:border-blue-500"
        >Express</a
      >
      for building api. I like backend development so much, so i&apos;m
      improving my backend skills into
      <a
        href="https://go.dev/"
        target="_blank"
        class="border-b border-dashed hover:text-blue-500 hover:border-blue-500"
        >Golang</a
      >
      with
      <a
        href="https://docs.gofiber.io/"
        target="_blank"
        class="border-b border-dashed hover:text-blue-500 hover:border-blue-500"
        >Fiber</a
      >
      framework
    </p>
    <div class="flex flex-wrap mt-6 gap-10">
      <img
        v-for="icon in icons"
        :src="icon"
        :alt="icon"
        class="cursor-pointer h-[25px] sm:h-[40px] hover:scale-125 transition duration-300"
      />
    </div>
  </div>
</template>
