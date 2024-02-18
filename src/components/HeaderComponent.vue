<template>
  <div class="header">
    <a
      class="header__item pc"
      href="#services"
      >Services</a
    >
    <a class="header__item pc">Benefits</a>
    <a class="header__item pc">Portfolio</a>
    <a class="header__item pc">Contacts</a>
    <div
      class="header__item tablet header__item--burger"
      @click="openBurger"
    >
      <svg
        v-if="!isBurgerOpened"
        width="50"
        height="50"
        viewBox="0 0 30 30"
        fill="none"
        xmlns="http://www.w3.org/2000/svg"
      >
        <circle
          cx="15"
          cy="15"
          r="15"
          fill="white"
        />
        <path
          d="M10 12H20"
          stroke="black"
          stroke-linecap="round"
        />
        <path
          d="M10 15H20"
          stroke="black"
          stroke-linecap="round"
        />
        <path
          d="M10 18H20"
          stroke="black"
          stroke-linecap="round"
        />
      </svg>
      <svg
        v-else
        width="50"
        height="50"
        viewBox="0 0 30 30"
        fill="none"
        xmlns="http://www.w3.org/2000/svg"
      >
        <circle
          cx="15"
          cy="15"
          r="15"
          fill="black"
        />
        <path
          d="M11 11L18.0711 18.0711"
          stroke="white"
          stroke-linecap="round"
        />
        <path
          d="M11 18.071L18.0711 11"
          stroke="white"
          stroke-linecap="round"
        />
      </svg>
    </div>
    <div
      class="burger-modal"
      v-if="isBurgerOpened"
    >
      <div class="burger-modal__content">
        <ul class="burger-modal__content__list">
          <li class="burger-modal__content__list__item"><a href="#">Services</a></li>
          <li class="burger-modal__content__list__item"><a href="#">Benefits</a></li>
          <li class="burger-modal__content__list__item"><a href="#">Portfolio</a></li>
          <li class="burger-modal__content__list__item"><a href="#">Contact</a></li>
          <li class="burger-modal__content__list__item--links">
            <GitSVG class="git" />
            <TelegramSVG class="tg" />
            <DiscrodSVG class="discord" />
          </li>
        </ul>
      </div>
    </div>
  </div>
</template>

<script setup>
  import {ref} from 'vue';
  import GitSVG from './icons/GitSVG.vue';
  import TelegramSVG from './icons/TelegramSVG.vue';
  import DiscrodSVG from './icons/DiscrodSVG.vue';

  const isBurgerOpened = ref(false);

  const openBurger = () => {
    isBurgerOpened.value = !isBurgerOpened.value;
    if (isBurgerOpened.value) {
      document.body.style.overflow = 'hidden';
    } else {
      document.body.style.overflow = '';
    }
  };
</script>

<style lang="scss" scoped>
  a {
    text-decoration: none;
    color: black;
  }

  .header {
    padding: var(--space-xl);
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

      &--burger {
        position: relative;
        z-index: 110;
      }
    }

    .pc {
      @include w-max($sm) {
        display: none;
      }
    }

    .tablet {
      @include w-min($sm) {
        display: none;
      }
    }
  }

  .burger-modal {
    display: flex;
    background-color: white;
    position: absolute;
    height: 100%;
    width: 120%;
    margin-top: -50px;
    margin-right: -50px;
    z-index: 100;

    &__content {
      display: flex;
      flex-direction: column;

      &__list {
        display: flex;
        flex-direction: column;
        align-items: start;
        justify-content: start;
        margin-left: 100px;
        margin-top: 100px;
        gap: 50px;

        &__item {
          font-family: var(--font-futura-bold);
          font-size: 30px;

          &--links {
            display: flex;
            flex-direction: row;
            align-items: center;
            justify-content: center;
            gap: 15px;

            svg {
              width: 40px;
              height: 40px;
            }

            ::v-deep(.git path:last-child) {
              fill: black;
            }

            ::v-deep(.tg path:last-child) {
              fill: black;
            }

            ::v-deep(.discord path:first-child) {
              fill: black;
            }

            ::v-deep(.discord path:last-child) {
              fill: white;
            }
          }
        }
      }
    }
  }
</style>
