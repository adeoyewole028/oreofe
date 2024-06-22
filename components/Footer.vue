<template>
  <div>
    <footer class="flex justify-between my-10">
      <h1>Ore-Ofe Oginni</h1>
      <div>
        <p>&copy; {{ currentYear }} Adegboyega</p>
      </div>
      <div class="flex gap-3">
     
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
