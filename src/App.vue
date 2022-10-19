<template>
  <AppHeader />
  <Pagination v-model:page="page" :pageLength="pageLength" />
</template>

<script setup lang="ts">
import { ref, provide, readonly } from 'vue';
import Pagination from './components/Pagination.vue';
import AppHeader from './components/AppHeader.vue';

const page = ref(1);
const pageLength = ref(10);

provide('tags', ['首頁', '關於我們', '聯繫我們']);
provide('page', readonly(page));
</script>

<style></style>
