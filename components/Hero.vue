<template>
  <div class="grid md:grid-cols-2 gap-y-5 mb-10 h-full">
    <div class="w-full flex flex-col justify-center items-start">
      <div class="text-start space-y-5">
        <img
          class="max-h-52 rounded-full object-fit"
          src="/img/abby.jpg"
          alt="Hero image"
        />
        <UBadge class="uppercase" color="white" size="lg" variant="solid"
          >Grace Oginni</UBadge
        >

        <h2 class="font-bold text-4xl md:text-7xl lg:text-8xl">
          Product Manager
        </h2>
      </div>
    </div>
    <div class="flex flex-col justify-end items-start">
      <p class="text-balance">
        Hi, I am Ore-Ofe – A goal driven Product Manager with a passion for
        researching, conceptualizing, and building scalable products that solve
        customer needs and achieve business objectives. Let us connect and
        collaborate
      </p>

      <div class="flex gap-3 mt-3">
        <div>
          <UButton>
            <a
              href="https://www.linkedin.com/in/oginni-grace-06b9a6163/?utm_source=share&utm_campaign=share_via&utm_content=profile&utm_medium=android_app"
            >
              Linkedin
            </a>
          </UButton>
        </div>
      </div>
    </div>
  </div>
</template>

<script lang="ts"></script>

<style scoped></style>
