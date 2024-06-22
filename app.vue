<template>
  <div class="container mx-auto px-5 md:px py-8">
    <NuxtLayout>
      <NuxtPage />
    </NuxtLayout>
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
