<template>
  <Pagination v-model="page" />
</template>

<script setup lang="ts">
import { ref } from 'vue';
import Pagination from './components/Pagination.vue';

const page = ref(1);
</script>

<style></style>
