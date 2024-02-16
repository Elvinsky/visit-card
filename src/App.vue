<template>
  <div
    class="container"
    id="root"
  >
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
    <div class="container__services">
      <ServiceComponent />
    </div>
    <div class="container__contact-form">
      <div class="container__contact-form--wrapper">
        <form
          class="container__contact-form--form"
          @submit.prevent
        >
          <h3>Contact Us</h3>
          <input
            type="text"
            placeholder="Name"
            name="name"
          />
          <input
            type="email"
            placeholder="Email"
            name="email"
          />
          <div class="container__contact-form__submit">Send</div>
        </form>
        <p class="container__contact-form--text">
          Ready to take your online presence to the next level? Contact us today for a free consultation. Let's turn your vision into a digital reality that captivates and converts.
        </p>
      </div>
      <div class="container__contact-form--logo">
        <svg
          width="618"
          height="538"
          viewBox="0 0 618 538"
          fill="none"
          xmlns="http://www.w3.org/2000/svg"
        >
          <path
            d="M0 353.066V272.362H12.1294C68.3936 272.362 124.658 272.144 180.96 272.653C213.758 272.944 238.471 260.111 251.621 231.392C264.506 203.291 259.707 176.245 239.68 151.888C230.8 140.982 225.078 132.984 216.5 121.897L219 121.895C221.296 121.464 213.087 122.047 215.421 121.897C246.293 121.897 277.202 121.533 308.074 121.897C310.46 122.104 312.78 122.763 314.901 123.836C317.021 124.909 318.9 126.375 320.43 128.15C373.86 196.202 341.779 306.025 259.367 338.088C255.588 339.506 252.112 341.106 246.784 343.287C271.156 374.26 287.82 409.558 319.221 433.333C331.985 442.776 346.822 449.291 362.6 452.382C403.107 460.053 438.173 446.457 466.853 419.01C517.789 370.552 538.647 311.042 529.352 243.425C520.207 177.117 485.973 125.06 421.622 95.6136C403.765 87.3104 384.309 82.6682 364.489 81.9812C273.272 80.5271 182.056 81.2177 90.8388 81.1813C88.3449 81.1813 85.8132 81.5813 81.9967 81.9085V227.611H0.0755316V0.513974H12.4317C122.806 0.513974 233.181 2.65882 343.48 0.0777553C476.073 -3.0486 579.91 88.5248 607.759 198.529C632.018 294.428 613.691 382.112 547.3 457.908C497.8 514.328 434.545 545.155 355.76 535.703C302.557 529.414 261.294 502.586 230.8 460.271C207.423 427.698 184.31 394.981 161.462 362.118C159.717 359.095 157.112 356.614 153.953 354.966C150.794 353.317 147.212 352.57 143.627 352.811C99.1518 353.32 54.6393 353.102 10.1268 353.138L0 353.066Z"
            fill="white"
          />
        </svg>
      </div>
    </div>
  </div>
</template>

<script setup>
  import HeaderComponent from '@/components/HeaderComponent.vue';
  import TextBlock from './components/TextBlock.vue';
  import ServiceComponent from './components/ServiceComponent.vue';
</script>

<style lang="scss" scoped>
  .container {
    background-color: black;
    padding: var(--space-2xl);
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    gap: 70px;
    position: relative;
    z-index: 1;
    margin-top: -820px;

    &__logo {
      font-size: 700px;
      text-shadow: var(--shadow-icon-main);
      font-family: var(--font-futura-bold);
      position: sticky;
      top: 0;
      z-index: -1;
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

    &__services {
      display: flex;
      flex-direction: column;
      align-items: center;
    }

    &__contact-form {
      display: flex;
      flex-direction: row;
      width: 70%;
      align-items: center;
      justify-content: space-between;
      height: fit-content;

      &--wrapper {
        display: flex;
        flex-direction: column;
        gap: 20px;
        height: 100%;
        justify-content: space-between;
      }

      h3 {
        font-family: var(--font-futura-bold);
        font-size: 48px;
        color: white;
      }

      &--text {
        font-family: var(--font-futura-regular);
        font-size: 32px;
        text-align: left;
        color: white;
      }

      &--form {
        padding: 20px 60px;
        display: flex;
        flex-direction: column;
        gap: 15px;
        border: 1px solid rgba(147, 147, 147, 1);
        border-radius: 20px;
        height: 100%;

        input {
          background-color: transparent;
          padding: 12px;
          color: rgba(147, 147, 147, 1);
          font-size: 16px;
          border: 1px solid rgba(147, 147, 147, 1);
          border-radius: 20px;
          width: 100%;
        }
      }
    }
  }
</style>

