<template>
  <div>
    <footer class="flex justify-between my-10">
      <NuxtLink to="/">Grace Oginni</NuxtLink>
      <div>
        <NuxtLink
          to="https://adegboyega-portfolio.netlify.app/"
          target="_blank"
        >
          &copy; {{ currentYear }}
          <span> Adegboyega </span>
        </NuxtLink>
      </div>
    </footer>
  </div>
</template>

<script lang="ts">
import { defineComponent } from "vue";

export default defineComponent({
  name: "Footer",
  setup() {
    return {
      currentYear: new Date().getFullYear(),
    };
  },
});
</script>

<style scoped></style>
