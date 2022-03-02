<template>
  <h2>Un titre d'article</h2>
  <button @click="emit('bigger', 2)">+</button>
  <button @click="emit('smaller')">-</button>
  <p :style="{ fontSize: props.fontSize + 'px' }">
    Lorem Ipsum is simply dummy text of the printing and typesetting industry.
    Lorem Ipsum has been the industry's standard dummy text ever since the
    1500s, when an unknown printer took a galley of type and scrambled it to
    make a type specimen book. It has survived not only five centuries, but also
    the leap into electronic typesetting, remaining essentially unchanged. It
    was popularised in the 1960s with the release of Letraset sheets containing
    Lorem Ipsum passages, and more recently with desktop publishing software
    like Aldus PageMaker including versions of Lorem Ipsum.
  </p>
</template>

<script setup lang="ts">
const props = defineProps<{ fontSize: Number }>();

const emit = defineEmits<{
  (e: 'bigger', inc: number): void;
  (e: 'smaller'): void;
}>();
</script>

<style scoped lang="scss"></style>
