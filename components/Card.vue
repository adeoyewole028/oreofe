<template>
  <component
    :is="cardTag"
    v-bind="cardAttrs"
    class="group block h-full rounded-2xl border p-4 transition duration-200"
    :class="
      hasPrimaryLink
        ? 'border-gray-300/70 bg-white/80 shadow-sm hover:-translate-y-1 hover:border-yellow-400 hover:shadow-lg focus-visible:outline-none focus-visible:ring-2 focus-visible:ring-yellow-400 focus-visible:ring-offset-2 focus-visible:ring-offset-white dark:border-gray-700 dark:bg-gray-900/70 dark:hover:border-yellow-400 dark:focus-visible:ring-offset-black'
        : 'border-gray-300/70 bg-white/80 shadow-sm dark:border-gray-700 dark:bg-gray-900/70'
    "
  >
    <div class="flex h-full flex-col gap-4 sm:flex-row sm:items-start">
      <div
        class="flex h-16 w-16 shrink-0 items-center justify-center rounded-2xl bg-yellow-400 sm:h-20 sm:w-20"
      >
        <i :class="icon" class="h-8 w-8 text-black sm:h-9 sm:w-9"></i>
      </div>
      <div class="flex min-w-0 flex-1 flex-col justify-between gap-3">
        <div class="space-y-2">
          <div class="flex items-start justify-between gap-3">
            <h3 class="text-lg font-semibold leading-tight text-gray-900 dark:text-white sm:text-xl">
              {{ title }}
            </h3>
            <span
              v-if="hasPrimaryLink"
              class="shrink-0 pt-1 text-[0.65rem] font-semibold uppercase tracking-[0.24em] text-yellow-500 transition duration-200 group-hover:translate-x-0.5"
            >
              Open
            </span>
          </div>
          <p class="text-sm leading-6 text-gray-600 dark:text-gray-400 sm:text-base">
            {{ description }}
          </p>
        </div>
        <!-- <p
          class="text-xs font-semibold uppercase tracking-[0.18em]"
          :class="hasPrimaryLink ? 'text-gray-500 dark:text-gray-400' : 'text-gray-400 dark:text-gray-500'"
        >
          {{ hasPrimaryLink ? "Tap anywhere on the card to open" : "Resource unavailable" }}
        </p> -->
      </div>
    </div>
  </component>
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
  computed: {
    primaryLink(): CardLink | null {
      return this.links[0] ?? null;
    },
    hasPrimaryLink(): boolean {
      return this.primaryLink !== null;
    },
    cardTag(): string {
      return this.hasPrimaryLink ? "a" : "div";
    },
    cardAttrs(): Record<string, string> {
      if (!this.primaryLink) {
        return {};
      }

      return {
        href: this.primaryLink.url,
        target: "_blank",
        rel: "noopener noreferrer",
        "aria-label": `Open ${this.title}`,
      };
    },
  },
});
</script>
