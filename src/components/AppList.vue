<template>
  <p>Now page: {{ page }}</p>
  <p>Active: {{ active() }}</p>
  <ul>
    <li v-for="(tag, index) in tags" :key="index">{{ tag }}</li>
  </ul>
</template>

<script setup lang="ts">
import { inject } from 'vue';

const tags = inject<string[]>('tags');
const page = inject<number>('page')!;
const active = inject<() => boolean>('active', () => false);
</script>

<style></style>
