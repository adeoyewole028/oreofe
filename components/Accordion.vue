<script setup lang="ts">
const items = [
  {
    label: "Product Manager - Giftawish",
    icon: "i-heroicons-rectangle-stack",
    content:
      "- Responsible for planning sprint for the design and development team - Responsible for writing User stories and user journeys to improve the product team's understanding of required features and functionalities - Work with cross functional teams to enhance a good user experience for the customers. - Worked with the marketing team to facilitate a great product marketing. -Assist the product lead to deliver good product services to our customers to facilitate a good user experience",
    defaultOpen: true,
  },
];
</script>

<template>
  <UAccordion class="mb-5 h-full" size="xl" :items="items" />
</template>
