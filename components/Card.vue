<template>
  <div class="border rounded-md border-gray-500 p-2 w-full h-full min-h-[8rem] flex">
    <div class="flex items-center w-full gap-3">
      <div
        class="bg-yellow-400 flex items-center justify-center max-h-20 w-20 h-20 rounded-md"
      >
        <i :class="icon" class="w-8 h-8 dark:text-black"></i>
      </div>
      <div class="w-full flex-1">
        <a
          v-if="links.length"
          :href="links[0].url"
          target="_blank"
          rel="noopener noreferrer"
          class="font-semibold text-xl underline-offset-4 transition hover:underline"
        >
          {{ title }}
        </a>
        <h3 v-else class="font-semibold text-xl">{{ title }}</h3>
        <p class="text-balance font-thin dark:text-gray-400">
          {{ description }}
        </p>
        <div v-if="links.length > 1" class="mt-3 flex flex-wrap gap-2">
          <a
            v-for="link in links.slice(1)"
            :key="link.url"
            :href="link.url"
            target="_blank"
            rel="noopener noreferrer"
            class="text-sm font-medium text-yellow-500 underline underline-offset-4 transition hover:text-yellow-400"
          >
            {{ link.label }}
          </a>
        </div>
      </div>
    </div>
  </div>
</template>

<script lang="ts">
import { defineComponent, type PropType } from "vue";

type CardLink = {
  label: string;
  url: string;
};

export default defineComponent({
  name: "Card",
  props: {
    title: {
      type: String,
      required: true,
    },
    description: {
      type: String,
      required: true,
    },
    icon: {
      type: String,
      required: true,
    },
    links: {
      type: Array as PropType<CardLink[]>,
      default: () => [],
    },
  },
});
</script>
