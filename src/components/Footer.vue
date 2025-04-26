<script setup lang="ts">
import Instagram from "/src/assets/social/instagram.png";
import Youtube from "/src/assets/social/youtube.png";
import Linkedin from "/src/assets/social/linkedin.png";
import Github from "/src/assets/social/github.png";
const icons = [
  { url: "https://www.youtube.com/@NoDegreeDeveloperOfficial", icon: Youtube },
  {
    url: "https://www.instagram.com/hanifrizq.15?igsh=YnhxamVqM3liNmVy",
    icon: Instagram,
  },
  { url: "https://www.linkedin.com/in/hanifahmadrizqullah/", icon: Linkedin },
  { url: "https://github.com/rizqiamad", icon: Github },
];

const currentYear = new Date().getFullYear();
</script>

<template>
  <footer class="text-white/90 max-w-[1200px] mx-auto px-4 relative">
    <nav
      class="flex flex-col tablet:flex-row tablet:justify-between gap-5 tablet:items-center py-4"
    >
      <p class="sm:text-base text-sm">
        <sup>&copy;</sup>{{ currentYear }} Hanif Ahmad Rizqullah, all right
        reserved
      </p>
      <div class="flex gap-6 flex-wrap justify-center">
        <a
          v-for="item in icons"
          target="_blank"
          :href="item.url"
          class="w-[40px] h-[40px] rounded-full flex justify-center items-center hover:bg-secondary cursor-pointer transition duration-300"
        >
          <img :src="item.icon" :alt="item.icon" width="25" height="25" />
        </a>
      </div>
    </nav>
  </footer>
</template>
