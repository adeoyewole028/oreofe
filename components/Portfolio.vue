<template>
  <div class="bg-yellow-400 p-5 lg:py-20 rounded-md space-y-5">
    <h1 class="dark:text-black text-3xl md:text-5xl font-bold">Portfolio</h1>
    <div class="grid md:grid-cols-2 w-full gap-3">
      <div
        v-for="port in portfolio"
        :key="port.id"
        class="group cursor-pointer"
      >
        <UCard class="relative">
          <template #header>
            <img
              class="rounded-md object-fit max-h-96 w-full transition duration-500 ease-in-out transform group-hover:translate-y-2 group-hover:scale-110 group-active:translate-y-2 group-active:scale-100"
              :src="port.img.src"
              :alt="port.img.alt"
            />
          </template>

          <template #footer>
            <div class="h-20">
              <h3 class="font-semibold text-xl">{{ port.title }}</h3>
              <p class="font-thin dark:text-gray-400">
                {{ port.description }}
              </p>
            </div>
          </template>
        </UCard>
      </div>
    </div>
  </div>
</template>

<script lang="ts">
import { defineComponent } from "vue";

export default defineComponent({
  name: "Portfolio",

  setup() {
    return {
      portfolio: [
        {
          id: 1,
          img: {
            src: "/img/abby.jpg",
            alt: "Hero image",
          },
          title: "User Research",
          description:
            "Research what user want and need to be able to complete",
        },
        {
          id: 2,
          img: {
            src: "/img/abby.jpg",
            alt: "Hero image",
          },
          title: "Wire-framing",
          description:
            "Create a visual guide that represents the skeletal framework of a website",
        },
        {
          id: 3,
          img: {
            src: "/img/abby.jpg",
            alt: "Hero image",
          },
          title: "Prototyping",
          description:
            "Create a prototype that can be used to test the product",
        },
      ],
    };
  },
});
</script>

<style scoped></style>
