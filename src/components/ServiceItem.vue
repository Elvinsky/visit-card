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
    min-width: 400px;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    gap: var(--space-l);
    padding: 1em;
    position: relative;

    @include w-max($sm) {
      width: 80%;
      min-width: 250px;
      margin: auto;
    }

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

      @include w-max($sm) {
        font-size: 20px;
        text-align: center;
      }
    }

    &__content {
      font-family: var(--font-futura-regular);
      font-size: var(--font-size-xl);
      color: rgb(202, 202, 202);

      @include w-max($sm) {
        font-size: 16px;
      }
    }
  }
</style>
