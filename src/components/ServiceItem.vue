<template>
  <fieldset class="service">
    <legend class="service__logo">
      <slot name="logo"></slot>
    </legend>
    <h3 class="service__header">
      <slot name="label"></slot>
    </h3>
    <p class="service__content">
      <slot name="content"></slot>
    </p>
  </fieldset>
</template>

<script setup></script>

<style scoped lang="scss">
  .service {
    border: 1px solid rgba(147, 147, 147, 1);
    border-radius: 20px;
    width: 100%;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    gap: var(--space-l);
    padding: 1em;
    position: relative;

    legend {
      margin: auto;
    }

    &__label,
    &__content {
      text-align: center;
    }

    &__header {
      font-family: var(--font-futura-bold);
      font-size: var(--font-size-3xl);
      color: white;
    }

    &__content {
      font-family: var(--font-futura-regular);
      font-size: var(--font-size-xl);
      color: rgb(202, 202, 202);
    }
  }
</style>
