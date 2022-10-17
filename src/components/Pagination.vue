<template>
  <button @click.prevent="emit('update:modelValue', modelValue - 1)">-</button>
  <span>{{ modelValue }}</span>
  <button @click.prevent="emit('update:modelValue', modelValue + 1)">+</button>
</template>

<script setup lang="ts">
const props = defineProps<{
  modelValue: number;
}>();

const emit = defineEmits<{
  (e: 'update:modelValue', page: number): void;
}>();
</script>

<style></style>
