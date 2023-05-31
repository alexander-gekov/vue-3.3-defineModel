<script setup lang="ts">
import { ref } from "vue";
import ChildNew from "./components/ChildNew.vue";
import ChildBefore from "./components/ChildBefore.vue";

const input = ref("This is initial input!");
</script>

<template>
  <div>Original Input:</div>
  <div>{{ input }}</div>
  <ChildNew v-model:input="input" />
  <ChildBefore v-model:input="input" />
</template>

<style scoped></style>
