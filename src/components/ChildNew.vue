<script setup lang="ts">
const input = defineModel<string>("input", {
  required: true,
});
</script>

<template>
  <div class="flex">
    <input v-model="input" type="text" />
    <button @click="input = ''">Clear</button>
  </div>
</template>

<style scoped></style>
