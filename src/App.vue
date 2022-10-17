<template>
  <Pagination v-model:page="page" :pageLength="pageLength" />
</template>

<script setup lang="ts">
import { ref } from 'vue';
import Pagination from './components/Pagination.vue';

const page = ref(1);
const pageLength = ref(10);
</script>

<style></style>
