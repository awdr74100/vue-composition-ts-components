<template>
  <button @click.prevent="emit('update:page', page - 1)" :disabled="page === 1">
    -
  </button>
  <ul>
    <li
      v-for="num in pageLength"
      :key="num"
      @click.prevent="emit('update:page', num)"
      :class="{ active: page === num }"
    >
      {{ num }}
    </li>
  </ul>
  <button
    @click.prevent="emit('update:page', page + 1)"
    :disabled="page === pageLength"
  >
    +
  </button>
</template>

<script setup lang="ts">
const props = defineProps<{
  page: number;
  pageLength: number;
}>();

const emit = defineEmits<{
  (e: 'update:page', page: number): void;
}>();
</script>

<style scoped>
ul li {
  border: 1px solid black;
  margin: 10px 0px;
  list-style: none;
  cursor: pointer;
}

.active {
  border-color: red;
}

button:disabled {
  cursor: not-allowed;
}
</style>
