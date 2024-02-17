<template>
  <div
    class="container"
    id="root"
  >
    <div class="container__logo">R</div>
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
      <ContactUsComponent />
    </div>
    <div class="container__resps">
      <div class="container__resps__wrapper">
        <div class="container__resps__wrapper__item">
          <div class="container__resps__wrapper__item__text-field">
            <h3>E-commerce Solutions</h3>
            <p>We understand that every business is unique. That's why we offer tailored solutions to meet your specific needs, ensuring your website reflects the essence of your brand.</p>
          </div>
          <div class="container__resps__wrapper__item__image">
            <img src="./assets/img/E-commerceSolutions.png" />
          </div>
        </div>
        <div class="container__resps__wrapper__item">
          <div class="container__resps__wrapper__item__text-field">
            <h3>Custom Website Development</h3>
            <p>
              Our team of skilled designers and developers work hand-in-hand to craft visually stunning and user-friendly websites. We stay ahead of the latest trends to ensure your website stands
              out.
            </p>
          </div>
          <div class="container__resps__wrapper__item__image">
            <img src="./assets/img/customDev.png" />
          </div>
        </div>
        <div class="container__resps__wrapper__item">
          <div class="container__resps__wrapper__item__text-field">
            <h3>Mobile App Development</h3>
            <p>Designing innovative and efficient mobile applications for both iOS and Android platforms to keep you connected with your audience on the go.</p>
          </div>
          <div class="container__resps__wrapper__item__image">
            <img src="./assets/img/mobileAppDevelopment.png" />
          </div>
        </div>
        <div class="container__resps__wrapper__item">
          <div class="container__resps__wrapper__item__text-field">
            <h3>Branding</h3>
            <p>Developing a strong, cohesive brand identity that effectively communicates your company's values and appeals to your target audience.</p>
          </div>
          <div class="container__resps__wrapper__item__image">
            <img src="./assets/img/branding.png" />
          </div>
        </div>
        <div class="container__resps__wrapper__item">
          <div class="container__resps__wrapper__item__text-field">
            <h3>Graphics Design</h3>
            <p>Producing visually stunning and impactful graphic designs for web and print, tailored to enhance your brand's messaging and aesthetic appeal.</p>
          </div>
          <div class="container__resps__wrapper__item__image">
            <img src="./assets/img/graphicsDesign.png" />
          </div>
        </div>
        <div class="container__resps__wrapper__item">
          <div class="container__resps__wrapper__item__text-field">
            <h3>Lorem Ipsum Dolor</h3>
            <p>
              Lorem ipsum dolor? Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate
            </p>
          </div>
          <div class="container__resps__wrapper__item__image">
            <img src="./assets/img/E-commerceSolutions.png" />
          </div>
        </div>
      </div>
    </div>
    <FooterComponent />
  </div>
</template>

<script setup>
  import HeaderComponent from '@/components/HeaderComponent.vue';
  import TextBlock from './components/TextBlock.vue';
  import ServiceComponent from './components/ServiceComponent.vue';
  import ContactUsComponent from './components/ContactUsComponent.vue';
  import FooterComponent from './components/FooterComponent.vue';
  import {ref, computed, onMounted} from 'vue';

  const shadowColorRed = ref(63);
  const shadowColorBlue = ref(154);

  const elementShadow = computed(() => `0px 0px 40px rgb(${shadowColorRed.value}, 221, ${shadowColorBlue.value})`);

  const scrollEvent = () => {
    const increment = 1;
    const maxValue = 255;

    shadowColorBlue.value = (shadowColorBlue.value + increment) % (maxValue + 1);
    shadowColorRed.value = (shadowColorRed.value + increment) % (maxValue + 1);
  };

  onMounted(() => {
    window.addEventListener('scroll', scrollEvent);
  });
</script>

<style lang="scss" scoped>
  .container {
    background-color: black;
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
      font-family: var(--font-futura-bold);
      position: sticky;
      top: 0;
      z-index: -1;
      color: black;
      display: flex;
      align-items: center;
      justify-content: center;
      width: 100%;
      text-shadow: v-bind(elementShadow);
      transition: all 0.3s ease;
    }

    &__text {
      padding: var(--space-2xl);

      display: flex;
      flex-direction: column;
      gap: 60px;
      width: 100%;

      &__item:last-child {
        align-self: flex-end;
      }
    }

    &__services {
      padding: var(--space-2xl);

      display: flex;
      flex-direction: column;
      align-items: center;
    }

    &__contact-form {
      padding: var(--space-2xl);

      display: flex;
      flex-direction: row;
      align-items: center;
      justify-content: center;
    }

    &__resps {
      padding: var(--space-2xl);

      display: flex;
      align-items: center;
      justify-content: center;
      width: 90%;

      &__wrapper {
        display: grid;
        place-items: center;
        grid-template-columns: 1fr 1fr;
        grid-template-rows: 1fr 1fr 1fr;
        gap: 50px;

        &__item {
          display: flex;
          flex-direction: row;
          justify-content: space-between;
          padding: 30px;
          border: 1px solid black;
          border-radius: 20px;
          box-shadow: 0px 0px 25px 0px rgba(255, 255, 255, 0.5);
          height: 300px;
          gap: 20px;

          &__text-field {
            display: flex;
            flex-direction: column;
            height: 100%;
            align-items: center;
            justify-content: space-around;
            gap: 15px;

            h3 {
              font-family: var(--font-futura-bold);
              color: white;
              font-size: 32px;
              text-align: start;
            }

            p {
              font-family: var(--font-futura-regular);
              color: #939393;
              font-size: 24px;
              text-align: start;
              text-decoration: green dashed;
            }
          }

          &__image {
            display: flex;
            align-items: center;
            justify-content: center;

            img {
              width: 150px;
            }
          }
        }
      }
    }
  }
</style>

