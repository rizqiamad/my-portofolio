<script lang="ts" setup>
import Html from "/programming-language/html.png";
import Css from "/programming-language/css.png";
import Javascript from "/programming-language/javascript.png";
import React from "/programming-language/react.png";
import Vue from "/programming-language/vue.png";
import Next from "/programming-language/nextjs.png";
import Tailwind from "/programming-language/tailwind.png";

const icons = [Html, Css, Javascript, React, Vue, Next, Tailwind];
</script>

<template>
  <div
    class="flex-1 lg:min-h-[23em] bg-secondary/20 p-4 rounded-xl border border-white/20"
  >
    <h2 class="font-semibold text-xl sm:text-2xl mb-4">Frontend</h2>
    <p class="sm:text-base text-sm">
      I'm able to implement simple design into great website using
      <a
        href="https://www.w3schools.com/html/"
        target="_blank"
        class="border-b border-dashed hover:text-blue-500 hover:border-blue-500"
        >Html</a
      >,
      <a
        href="https://www.w3schools.com/css/"
        target="_blank"
        class="border-b border-dashed hover:text-blue-500 hover:border-blue-500"
        >Css</a
      >
      and
      <a
        href="https://www.typescriptlang.org/"
        target="_blank"
        class="border-b border-dashed hover:text-blue-500 hover:border-blue-500"
        >Typescript</a
      >
      strongly typed version of
      <a
        href="https://www.w3schools.com/js/default.asp"
        target="_blank"
        class="border-b border-dashed hover:text-blue-500 hover:border-blue-500"
        >Javascript</a
      >
      with some frameworks like
      <a
        href="https://react.dev/"
        target="_blank"
        class="border-b border-dashed hover:text-blue-500 hover:border-blue-500"
        >React</a
      >,
      <a
        href="https://vuejs.org/"
        target="_blank"
        class="border-b border-dashed hover:text-blue-500 hover:border-blue-500"
        >Vue</a
      >,
      <a
        href="https://nextjs.org/"
        target="_blank"
        class="border-b border-dashed hover:text-blue-500 hover:border-blue-500"
        >Next</a
      >
      and
      <a
        href="https://tailwindcss.com/"
        target="_blank"
        class="border-b border-dashed hover:text-blue-500 hover:border-blue-500"
        >Tailwind</a
      >
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
