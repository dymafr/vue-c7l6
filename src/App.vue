<template>
  <Blog @bigger="incSize" @smaller="fontSize--" :fontSize="fontSize" />
  <Blog @bigger="incSize" @smaller="fontSize--" :fontSize="fontSize" />
</template>

<script setup lang="ts">
import { ref } from 'vue';
import Blog from './Blog.vue';

const fontSize = ref(12);

function incSize(inc: number) {
  fontSize.value += inc;
}
</script>

<style scoped lang="scss"></style>
