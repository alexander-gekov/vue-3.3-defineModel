<script setup lang="ts">
import { computed } from "vue";

const props = defineProps({
  input: {
    type: String,
    required: true,
  },
});

const emit = defineEmits(["update:input"]);

const input = computed({
  get: () => props.input,
  set: (value) => emit("update:input", value),
});
</script>

<template>
  <div class="flex">
    <input :value="input" type="text" />
    <button @click="input = ''">Clear</button>
  </div>
</template>

<style scoped></style>
