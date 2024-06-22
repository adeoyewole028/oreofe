<template>
  <div class="space-y-5">
    <h1 class="text-3xl md:text-5xl font-bold">Let's Collaborate</h1>
    <div class="grid lg:grid-cols-3 gap-5 w-full">
      <div v-for="info in personalInfo" :key="info.id">
        <div class="border rounded-md border-gray-500 p-5 w-full  flex">
          <div class="flex items-center justify-between w-full">
            <div class="w-full flex-1">
              <h3 class="font-semibold text-xl">{{ info.title }}</h3>
              <p class="text-balance font-thin dark:text-gray-400">
                {{ info.description }}
              </p>
            </div>
            <i :class="info.icon"></i>
          </div>
        </div>
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
          description: "abby@gmail.com",
          icon: "i-heroicons-envelope",
        },

        {
          id: 2,
          title: "Linkedin",
          description: "linkedin.com/abby",
          icon: "i-heroicons-linkedin",
        },
        {
          id: 3,
          title: "Twitter",
          description: "twitter.com/abby",
          icon: "i-heroicons-twitter",
        },
      ],
    };
  },
});
</script>

<style scoped></style>
