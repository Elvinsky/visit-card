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
              <img
                src="../assets/img/cutting-edge.png"
                width="170"
              />
            </template>
            <template #label>Cutting-Edge Design</template>
            <template #content>
              Our team of skilled designers and developers work hand-in-hand to craft visually stunning and user-friendly websites. We stay ahead of the latest trends to ensure your website stands
              out.
            </template>
          </ServiceItem>
        </div>
        <div class="services__wrapper__item">
          <ServiceItem>
            <template #logo>
              <img
                src="../assets/img/solutions.png"
                width="170"
              />
            </template>
            <template #label>Cutting-Edge Design</template>
            <template #content>
              Our team of skilled designers and developers work hand-in-hand to craft visually stunning and user-friendly websites. We stay ahead of the latest trends to ensure your website stands
              out.
            </template>
          </ServiceItem>
        </div>
        <div class="services__wrapper__item">
          <ServiceItem>
            <template #logo>
              <img
                src="../assets/img/rda.png"
                width="170"
              />
            </template>
            <template #label>Cutting-Edge Design</template>
            <template #content>
              Our team of skilled designers and developers work hand-in-hand to craft visually stunning and user-friendly websites. We stay ahead of the latest trends to ensure your website stands
              out.
            </template>
          </ServiceItem>
        </div>
      </div>
      <div class="services__wrapper--secondline">
        <div class="services__wrapper__item">
          <ServiceItem>
            <template #logo>
              <img
                src="../assets/img/ux.png"
                width="170"
              />
            </template>
            <template #label>Cutting-Edge Design</template>
            <template #content>
              Our team of skilled designers and developers work hand-in-hand to craft visually stunning and user-friendly websites. We stay ahead of the latest trends to ensure your website stands
              out.
            </template>
          </ServiceItem>
        </div>
        <div class="services__wrapper__item">
          <ServiceItem>
            <template #logo>
              <img
                src="../assets/img/support.png"
                width="170"
              />
            </template>
            <template #label>Cutting-Edge Design</template>
            <template #content>
              Our team of skilled designers and developers work hand-in-hand to craft visually stunning and user-friendly websites. We stay ahead of the latest trends to ensure your website stands
              out.
            </template>
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
  .services {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    gap: var(--space-5xl);
    width: 80%;

    &__header {
      color: white;
      font-family: var(--font-futura-bold);
      font-size: 48px;
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
      }
    }
  }
</style>
