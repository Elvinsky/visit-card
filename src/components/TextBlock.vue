<template>
  <p class="text">
    <slot></slot>
  </p>
</template>

<script setup>
  defineProps({
    color: {
      type: String,
      default: 'white',
    },
    align: {
      type: String,
      default: 'center',
    },
    fontSize: {
      type: String,
      default: '24px',
    },
    width: {
      type: String,
      default: '100%',
    },
  });
</script>

<style lang="scss" scoped>
  .text {
    color: v-bind(color);
    font-size: v-bind(fontSize);
    width: v-bind(width);
    text-align: v-bind(align);
    font-family: var(--font-futura-regular);
  }
</style>
