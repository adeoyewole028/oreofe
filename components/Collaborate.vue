<template>
  <div class="space-y-5">
    <h1 class="text-3xl md:text-5xl font-bold">Let's Collaborate</h1>
    <div class="grid lg:grid-cols-3 gap-5 w-full">
      <div v-for="info in personalInfo" :key="info.id">
        <NuxtLink
          v-if="info.title === 'Email'"
          :to="'mailto:' + info.link"
          target="_blank"
          class="border rounded-md border-gray-500 p-5 w-full flex"
        >
          <div class="flex items-center justify-between w-full">
            <div class="w-full flex-1">
              <h3 class="font-semibold text-xl">{{ info.title }}</h3>

              <p class="text-balance font-thin dark:text-gray-400">
                {{ info.name }}
              </p>
            </div>
            <i :class="info.icon"></i>
          </div>
        </NuxtLink>
        <NuxtLink
          v-else
          :to="info.link"
          target="_blank"
          class="border rounded-md border-gray-500 p-5 w-full flex"
        >
          <div class="flex items-center justify-between w-full">
            <div class="w-full flex-1">
              <h3 class="font-semibold text-xl">{{ info.title }}</h3>

              <p class="text-balance font-thin dark:text-gray-400">
                {{ info.name }}
              </p>
            </div>
            <i :class="info.icon"></i>
          </div>
        </NuxtLink>
      </div>
    </div>
  </div>
</template>

<script lang="ts">
import { defineComponent } from "vue";

export default defineComponent({
  name: "Collaborate",

  setup() {
    return {
      personalInfo: [
        {
          id: 1,
          title: "Email",
          name: "graceoginni89@gmail.com",
          link: "graceoginni89@gmail.com",
          icon: "i-heroicons-envelope",
        },

        {
          id: 2,
          title: "Linkedin",
          name: "Grace Oginni",
          link: "https://www.linkedin.com/in/oginni-grace-06b9a6163?utm_source=share&utm_campaign=share_via&utm_content=profile&utm_medium=android_app",
          icon: "i-heroicons-linkedin",
        },
        {
          id: 3,
          title: "Twitter",
          name: "@abby_oreofee",
          link: "https://twitter.com/abby_oreofee",
          icon: "i-heroicons-twitter",
        },
      ],
    };
  },
});
</script>

<style scoped></style>
