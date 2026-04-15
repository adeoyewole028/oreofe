<template>
  <div class="space-y-5">
    <h1 class="text-3xl md:text-5xl font-bold">Skills</h1>
    <div class="grid w-full auto-rows-fr gap-4 sm:grid-cols-2 xl:grid-cols-3">
      <div v-for="skill in skills" :key="skill.id" class="h-full">
        <Card
          :title="skill.title"
          :description="skill.description"
          :icon="skill.icon"
          :links="skill.links"
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
    links: [
      {
        label: "User Research",
        url: "https://docs.google.com/spreadsheets/d/1kidT9EJKFs2i7JORNXIjW61cfXNp5-ZKEc9O_X5gtgg/edit?gid=374003723#gid=374003723",
      },
    ],
  },
  {
    id: 2,
    title: "Wire-framing",
    description:
      "Create a visual guide that represents the skeletal framework of a website",
    icon: "i-heroicons-pencil",
    links: [
      {
        label: "Wire-framing",
        url: "https://whimsical.com/oginni/giftawish-sketch-EMsSGgwnEA4VA5vQ7gjU4k",
      },
    ],
  },
  {
    id: 3,
    title: "Prototyping",
    description: "Create a prototype that can be used to test the product",
    icon: "i-heroicons-cube",
    links: [
      {
        label: "Prototyping",
        url: "https://www.figma.com/design/F9znkGD1PknjKzuKbLiE8n/giftawish?node-id=0-1&t=bEjBdoFvtAipHnNT-1",
      },
    ],
  },
  {
    id: 4,
    title: "User Testing",
    description: "Test the product with users to see if it meets their needs",
    icon: "i-heroicons-user-plus",
    links: [],
  },
  {
    id: 5,
    title: "Project Management",
    description: "Coordinate planning, execution, and delivery across the project lifecycle",
    icon: "i-heroicons-cog",
    links: [
      {
        label: "Project Management",
        url: "https://app.clickup.com/9005180305/v/li/900502540523",
      },
    ],
  },
  {
    id: 6,
    title: "Product Strategy",
    description:
      "Create a strategy for the product that aligns with the business goals",
    icon: "i-heroicons-chart-pie",
    links: [
      {
        label: "Product Strategy",
        url: "https://docs.google.com/document/d/1ejp5W48M0C5MF6CvhzH3pcF-BaGOOotb/edit",
      },
    ],
  },
  {
    id: 7,
    title: "Road mapping",
    description:
      "Plan delivery milestones and priorities to keep the product moving forward",
    icon: "i-heroicons-map",
    links: [
      {
        label: "Road mapping",
        url: "https://ituidsa-my.sharepoint.com/:w:/g/personal/grace-oluwatosin_oginni_students_it-u_at/IQA-IovVyxVRRovPiY6-diquAWTJxMvCQlRh32NCqVdOFSY?rtime=dKtXv96a3kg",
      },
    ],
  },
];
</script>

<style scoped></style>
