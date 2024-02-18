<template>
  <div class="footer">
    <div class="footer__logo">
      <LogoSVG />
    </div>
    <nav class="footer__nav">
      <a
        class="footer__nav__item"
        href="#"
      >
        Services
      </a>
      <a
        class="footer__nav__item"
        href="#"
      >
        Benefits
      </a>
      <a
        class="footer__nav__item"
        href="#"
      >
        Portfolio
      </a>
      <a
        class="footer__nav__item"
        href="#"
      >
        Contact
      </a>
    </nav>
    <nav class="footer__social">
      <a
        class="footer__social__item"
        href="#"
      >
        <GitSVG />
      </a>
      <a
        class="footer__social__item"
        href="#"
      >
        <TelegramSVG />
      </a>
      <a
        class="footer__social__item"
        href="#"
      >
        <DiscrodSVG />
      </a>
    </nav>
  </div>
</template>

<script setup>
  import LogoSVG from './icons/LogoSVG.vue';
  import TelegramSVG from './icons/TelegramSVG.vue';
  import GitSVG from './icons/GitSVG.vue';
  import DiscrodSVG from './icons/DiscrodSVG.vue';
</script>

<style scoped lang="scss">
  a {
    text-decoration: none;
    color: white;
    font-family: var(--font-futura-bold);
    font-size: 24px;
    transition: all 0.3s ease;

    &:hover {
      cursor: pointer;
      color: #939393;
    }
  }

  .footer {
    display: flex;
    flex-direction: row;
    width: 100%;
    position: sticky;
    bottom: 0;
    border-top: 1px solid white;
    padding: 10px 20px;
    align-items: center;
    justify-content: space-between;
    background-color: black;
    left: 0;
    right: 0;

    &__nav {
      display: flex;
      flex-direction: row;
      gap: 100px;
      align-items: center;
      justify-content: center;
    }

    &__social {
      display: flex;
      flex-direction: row;
      align-items: center;
      justify-content: center;
      gap: 30px;
    }

    @include w-max($lg) {
      flex-direction: column;
      justify-content: center;
      gap: 15px;
      position: static;

      &__nav {
        flex-direction: column;
        gap: 20px;
      }

      &__social {
        gap: 15px;

        svg {
          width: 30px;
          height: 30px;
        }
      }
    }
  }
</style>
