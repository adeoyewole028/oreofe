<template>
  <div>
    <nav class="flex justify-between mb-10">
      <h1 class="text-2xl md:text-4xl font-bold">Grace Oginni</h1>
      <div class="flex gap-3">
        <UButton>
          <nuxt-link
            target="_blank"
            to="https://www.linkedin.com/in/oginni-grace-06b9a6163/?utm_source=share&utm_campaign=share_via&utm_content=profile&utm_medium=android_app"
            >Linkedin</nuxt-link
          >
        </UButton>
        <UButton class="hidden md:block">
          <nuxt-link to="mailto:graceoginni89@gmail.com">Email</nuxt-link>
        </UButton>
        <UButton icon="i-heroicons-moon" @click="toggleColorMode"></UButton>
      </div>
    </nav>
  </div>
</template>

<script>

export default {
  methods: {
    toggleColorMode() {
      this.$colorMode.preference =
        this.$colorMode.preference === "dark" ? "light" : "dark";
    },
  },
};
</script>

<style scoped></style>
