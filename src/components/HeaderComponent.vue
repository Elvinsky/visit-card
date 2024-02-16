<template>
  <div class="header">
    <a
      class="header__item"
      href="#services"
      >Services</a
    >
    <a class="header__item">Benefits</a>
    <a class="header__item">Portfolio</a>
    <a class="header__item">Contacts</a>
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
      transition: all 0.3s ease;

      &:hover {
        color: white;
        cursor: pointer;
      }
    }
  }
</style>
