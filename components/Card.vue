<template>
  <div class="border rounded-md border-gray-500 p-2 w-full h-32 flex">
    <div class="flex items-center w-full gap-3">
      <div class="bg-yellow-400 flex items-center justify-center max-h-20 w-20 h-20 rounded-md">
        <!-- <img
          class="max-h-20 rounded-full object-fit"
          src="/img/abby.jpg"
          alt="Hero image"
        /> -->
        <i :class="icon" class="w-8 h-8 dark:text-black"></i>
      </div>
      <div class="w-full flex-1">
        <h3 class="font-semibold text-xl">{{ title }}</h3>
        <p class="text-balance font-thin dark:text-gray-400">
          {{ description }}
        </p>
      </div>
    </div>
  </div>
</template>

<script lang="ts">
import { defineComponent } from "vue";

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
  },

  setup() {
    return {};
  },
});
</script>
