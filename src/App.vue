<template>
  <div class="container">
    <p class="container__logo">R</p>
    <HeaderComponent />
    <div class="container__text">
      <TextBlock
        font-size="48px"
        width="30vw"
        align="start"
        class="container__text__item"
      >
        “Resolute devs” - is a team of professionals specializing in creating websites with maximum speed and quality.
      </TextBlock>
      <TextBlock
        font-size="48px"
        width="30vw"
        align="start"
        class="container__text__item"
      >
        We offer a full range of services for the development, maintenance and promotion of websites, mobile applications and software.
      </TextBlock>
    </div>
  </div>
</template>

<script setup>
  import HeaderComponent from '@/components/HeaderComponent.vue';
  import TextBlock from './components/TextBlock.vue';
</script>

<style lang="scss" scoped>
  .container {
    background-color: black;
    padding: var(--space-2xl);
    display: flex;
    flex-direction: column;
    gap: var(--space-5xl);
    position: relative;
    z-index: 1;
    margin-top: -920px;

    &__logo {
      font-size: 800px;
      text-shadow: var(--shadow-icon-main);
      font-family: var(--font-futura-bold);
      position: sticky;
      top: 0;
      z-index: -9;
      color: rgb(73, 73, 73);
      display: flex;
      align-items: center;
      justify-content: center;
      width: 100%;
    }

    &__text {
      display: flex;
      flex-direction: column;
      gap: 60px;
      width: 100%;

      &__item:last-child {
        align-self: flex-end;
      }
    }
  }
</style>

