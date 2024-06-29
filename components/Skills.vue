<template>
  <div class="space-y-5">
    <h1 class="text-3xl md:text-5xl font-bold">Skills</h1>
    <div class="grid lg:grid-cols-3 gap-5 w-full">
      <div v-for="skill in skills" :key="skill.id">
        <Card
          :title="skill.title"
          :description="skill.description"
          :icon="skill.icon"
        />
      </div>
    </div>
  </div>
</template>

<script lang="ts" setup>
const skills = [
  {
    id: 1,
    title: "User Research",
    description: "Gathering feedbacks from users  to understand their pain-points.",
    icon: "i-heroicons-user-group",
  },
  {
    id: 2,
    title: "Wire-framing",
    description:
      "Create a visual guide that represents the skeletal framework of a website",
    icon: "i-heroicons-pencil",
  },
  {
    id: 3,
    title: "Prototyping",
    description: "Create a prototype that can be used to test the product",
    icon: "i-heroicons-cube",
  },
  {
    id: 4,
    title: "User Testing",
    description: "Test the product with users to see if it meets their needs",
    icon: "i-heroicons-user-plus",
  },
  {
    id: 5,
    title: "Product Management",
    description: "Manage the product from conception to launch",
    icon: "i-heroicons-cog",
  },
  {
    id: 6,
    title: "Product Strategy",
    description:
      "Create a strategy for the product that aligns with the business goals",
    icon: "i-heroicons-chart-pie",
  },
];
</script>

<style scoped></style>
