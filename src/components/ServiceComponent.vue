<template>
  <div
    class="services"
    id="services"
  >
    <h2 class="services__header">Our Services</h2>
    <div class="services__wrapper">
      <div class="services__wrapper--firstline">
        <div class="services__wrapper__item">
          <ServiceItem>
            <template #logo>
              <img src="../assets/img/cutting-edge.png" />
            </template>
            <template #label>Cutting-Edge Design</template>
            <template #content>
              We understand that every business is unique. That's why we offer tailored solutions to meet your specific needs, ensuring your website reflects the essence of your brand.
            </template>
          </ServiceItem>
        </div>
        <div class="services__wrapper__item">
          <ServiceItem>
            <template #logo>
              <img src="../assets/img/solutions.png" />
            </template>
            <template #label>Customized Solutions</template>
            <template #content>
              Our team of skilled designers and developers work hand-in-hand to craft visually stunning and user-friendly websites. We stay ahead of the latest trends to ensure your website stands
              out.
            </template>
          </ServiceItem>
        </div>
        <div class="services__wrapper__item">
          <ServiceItem>
            <template #logo>
              <img src="../assets/img/rda.png" />
            </template>
            <template #label>Results-Driven Approach</template>
            <template #content> Our goal is to not just launch websites, but to create platforms that drive growth. From SEO optimization to responsive design </template>
          </ServiceItem>
        </div>
      </div>
      <div class="services__wrapper--secondline">
        <div class="services__wrapper__item">
          <ServiceItem>
            <template #logo>
              <img src="../assets/img/ux.png" />
            </template>
            <template #label>Seamless User Experience</template>
            <template #content> We prioritize usability in every project. By focusing on intuitive navigation and fast load times, we ensure a smooth experience for all your visitors. </template>
          </ServiceItem>
        </div>
        <div class="services__wrapper__item">
          <ServiceItem>
            <template #logo>
              <img src="../assets/img/support.png" />
            </template>
            <template #label>Ongoing Support</template>
            <template #content> Launching your website is just the beginning. We provide ongoing maintenance and support to keep your site up-to-date and performing at its best. </template>
          </ServiceItem>
        </div>
      </div>
    </div>
  </div>
</template>
<script setup>
  import ServiceItem from './ServiceItem.vue';
</script>
<style lang="scss" scoped>
  img {
    width: 170px;

    @include w-max($sm) {
      width: 80px;
    }
  }
  .services {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    gap: var(--space-5xl);
    width: 90%;

    &__header {
      color: white;
      font-family: var(--font-futura-bold);
      font-size: 48px;

      @include w-max($sm) {
        font-size: 20px;
      }
    }

    &__wrapper {
      display: flex;
      flex-direction: column;
      gap: 40px;

      &--firstline,
      &--secondline {
        display: flex;
        flex-direction: row;
        gap: 40px;

        @include w-max($lg) {
          flex-direction: column;
        }
      }
    }
  }
</style>
