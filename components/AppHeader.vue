<template>
  <div>
    <nav class="flex justify-between mb-10">
      <h1>Grace Oginni</h1>
      <div class="flex gap-3">
        <UButton>
          <nuxt-link to="/">Linkedin</nuxt-link>
        </UButton>
        <UButton>
          <nuxt-link to="/">Email</nuxt-link>
        </UButton>
        <UButton icon="i-heroicons-moon" @click="toggleColorMode"
          ></UButton>
        
      </div>
    </nav>
  </div>
</template>

<script>
export default {
  methods: {
    toggleColorMode() {
      this.$colorMode.preference = this.$colorMode.preference === 'dark' ? 'light' : 'dark'
    }
  }
}
</script>

<style scoped></style>
