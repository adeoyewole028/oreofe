<script setup lang="ts">
const items = [
  {
    label: "Product Manager",
    icon: "i-heroicons-rectangle-stack",
    defaultOpen: true,
    content:
      "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed neque elit, tristique placerat feugiat ac, facilisis vitae arcu. Proin eget egestas augue. Praesent ut sem nec arcu pellentesque aliquet. Duis dapibus diam vel metus tempus vulputate.",
  },

  {
    label: "Product Manager",
    icon: "i-heroicons-rectangle-stack",
    content:
      "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed neque elit, tristique placerat feugiat ac, facilisis vitae arcu. Proin eget egestas augue. Praesent ut sem nec arcu pellentesque aliquet. Duis dapibus diam vel metus tempus vulputate.",
  },
];
</script>

<template>
  <UAccordion class="mb-5 h-full" size="xl" :items="items" />
</template>
