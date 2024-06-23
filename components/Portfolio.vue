<template>
  <div class="bg-yellow-400 p-5 lg:py-20 rounded-md space-y-5">
    <h1 class="dark:text-black text-3xl md:text-5xl font-bold">Portfolio</h1>
    <div class="grid md:grid-cols-2 w-full gap-3">
      <div
        v-for="port in portfolio"
        :key="port.id"
        class="rounded-md group relative bg-black"
      >
        <div class="relative overflow-hidden md:h-96 w-full p-5">
          <img
            class="rounded-md object-cover h-full w-full transition duration-500 ease-in-out transform group-hover:-scale-x-100"
            :src="port.img.src"
            :alt="port.img.alt"
          />
          <div
            class="absolute inset-0 bg-black bg-opacity-70 flex flex-col gap-5 justify-center items-center opacity-0 group-hover:opacity-100 transition duration-500 ease-in-out transform group-hover:rotate-y-0"
          >
            <NuxtLink
              v-if="port.link"
              :to="port.link"
              target="_blank"
              class="text-white text-lg flex items-center gap-2 focus:outline-none disabled:cursor-not-allowed disabled:opacity-75 flex-shrink-0 font-medium rounded-md text-sm gap-x-1.5 px-2.5 py-1.5 shadow-sm text-white dark:text-gray-900 bg-primary-500 hover:bg-primary-600 disabled:bg-primary-500 dark:bg-primary-400 dark:hover:bg-primary-500 dark:disabled:bg-primary-400 focus-visible:outline focus-visible:outline-2 focus-visible:outline-offset-2 focus-visible:outline-primary-500 dark:focus-visible:outline-primary-400 inline-flex items-center"
            >
              <i class="i-heroicons-globe-alt"></i>
              <span> - Live</span>
            </NuxtLink>
            <NuxtLink
              v-if="port.docLink"
              :to="port.docLink"
              target="_blank"
              class="text-white text-lg focus:outline-none disabled:cursor-not-allowed disabled:opacity-75 flex-shrink-0 font-medium rounded-md text-sm gap-x-1.5 px-2.5 py-1.5 shadow-sm text-white dark:text-gray-900 bg-primary-500 hover:bg-primary-600 disabled:bg-primary-500 dark:bg-primary-400 dark:hover:bg-primary-500 dark:disabled:bg-primary-400 focus-visible:outline focus-visible:outline-2 focus-visible:outline-offset-2 focus-visible:outline-primary-500 dark:focus-visible:outline-primary-400 inline-flex items-center"
            >
              {{ port.title }} - PRD
            </NuxtLink>
            <NuxtLink
              v-if="port.strategyLink"
              :to="port.strategyLink"
              target="_blank"
              class="text-white text-lg focus:outline-none disabled:cursor-not-allowed disabled:opacity-75 flex-shrink-0 font-medium rounded-md text-sm gap-x-1.5 px-2.5 py-1.5 shadow-sm text-white dark:text-gray-900 bg-primary-500 hover:bg-primary-600 disabled:bg-primary-500 dark:bg-primary-400 dark:hover:bg-primary-500 dark:disabled:bg-primary-400 focus-visible:outline focus-visible:outline-2 focus-visible:outline-offset-2 focus-visible:outline-primary-500 dark:focus-visible:outline-primary-400 inline-flex items-center"
            >
              {{ port.title }} - Strategy
            </NuxtLink>
          </div>
        </div>
        <div class="mt-3 p-5">
          <NuxtLink
            :to="port.link"
            target="_blank"
            class="font-semibold text-xl"
            >{{ port.title }}</NuxtLink
          >
          <NuxtLink
            :to="port.docLink"
            target="_blank"
            class="font-thin dark:text-gray-400 text-white"
          >
            <p>{{ port.description }}</p>
          </NuxtLink>
        </div>
      </div>
    </div>
  </div>
</template>

<script lang="ts" setup>
const portfolio = [
  {
    id: 1,
    img: {
      src: "/img/giftawish.png",
      alt: "Gift A Wish",
    },
    title: "Gift A Wish",
    description:
      "Giftawish is a revolutionary social networking and e-commerce platform dedicated to facilitating the seamless exchange of gifts among loved ones",
    link: "https://giftawish.vercel.app/",
    docLink:
      "https://docs.google.com/document/d/1ejp5W48M0C5MF6CvhzH3pcF-BaGOOotb/edit",
    strategyLink:
      "https://docs.google.com/document/d/163C2V5yTc-QCWf5PW9EoiWxyFB3xC4Vp/edit",
  },
  {
    id: 2,
    img: {
      src: "/img/jumia.png",
      alt: "Jumia",
    },
    title: "JUMIA App case study",
    description: "A Product teardown of the Jumia app",
    docLink:
      "https://docs.google.com/presentation/d/1o4ExPzFRfYen9aVzTdWFmUFn0XeyI7I2/edit#slide=id.p1",
  },
];
</script>

<style scoped>
/* .group-hover\:rotate-y-180 {
  transform: rotateY(180deg);
}
.group-hover\:rotate-y-0 {
  transform: rotateY(0);
}
.rotate-y-180 {
  transform: rotateY(180deg);
} */
</style>
