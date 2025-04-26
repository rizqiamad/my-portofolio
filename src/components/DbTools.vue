<script lang="ts" setup>
import Mongodb from "/src/assets/db/mongodb.png";
import Postgresql from "/src/assets/db/postgresql.png";
import Git from "/src/assets/tools/git.png";
import Github from "/src/assets/tools/github.png";
import Mongoose from "/src/assets/tools/mongoose.png";
import Prisma from "/src/assets/tools/prisma.png";

const icons = [Mongodb, Postgresql, Git, Github, Mongoose, Prisma];
</script>

<template>
  <div
    class="flex-1 lg:min-h-[23em] bg-secondary/20 p-4 rounded-xl border border-white/20"
  >
    <h2 class="font-semibold text-xl sm:text-2xl mb-4">Databases and tools</h2>
    <p class="sm:text-base text-sm">
      These are the databases and tools that i&apos;ve ever used for building
      website as a storage of web data. I used
      <a
        href="https://www.postgresql.org/"
        target="_blank"
        class="border-b border-dashed hover:text-blue-500 hover:border-blue-500"
        >Postgresql</a
      >
      and
      <a
        href="https://www.mongodb.com/"
        target="_blank"
        class="border-b border-dashed hover:text-blue-500 hover:border-blue-500"
        >Mongodb</a
      >
      for databases. I never forget to use the tools to assist every development
      such as
      <a
        href="https://www.prisma.io/"
        target="_blank"
        class="border-b border-dashed hover:text-blue-500 hover:border-blue-500"
        >Prisma</a
      >,
      <a
        href="https://mongoosejs.com/"
        target="_blank"
        class="border-b border-dashed hover:text-blue-500 hover:border-blue-500"
        >Mongoose</a
      >,
      <a
        href="https://git-scm.com/downloads"
        target="_blank"
        class="border-b border-dashed hover:text-blue-500 hover:border-blue-500"
        >Git</a
      >
      and
      <a
        href="https://github.com/"
        target="_blank"
        class="border-b border-dashed hover:text-blue-500 hover:border-blue-500"
        >Github</a
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
