<template>
  <div class="header">
    <div class="header__item">Services</div>
    <div class="header__item">Benefits</div>
    <div class="header__item">Portfolio</div>
    <div class="header__item">Contacts</div>
  </div>
</template>
<style lang="scss" scoped>
  .header {
    display: flex;
    flex-direction: row;
    width: 100%;
    justify-content: end;
    gap: var(--space-3xl);

    &__item {
      color: var(--font-color-secondary);
      font-family: var(--font-futura-bold);
      font-size: var(--font-size-xl);
    }
  }
</style>
