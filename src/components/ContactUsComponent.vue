<template>
  <div class="contact-form">
    <div class="contact-form__first-part">
      <form
        class="contact-form__first-part__form"
        @submit.prevent
      >
        <h3 class="contact-form__first-part__form__header">Contact Us</h3>
        <input
          type="text"
          name="name"
          placeholder="Name"
          id="name"
          v-model="formData.name"
        />
        <input
          type="email"
          name="email"
          placeholder="Email"
          id="email"
          v-model="formData.email"
        />
        <div
          class="contact-form__first-part__form__submit"
          @click="handleSendForm"
        >
          Send
        </div>
      </form>
      <div class="contact-form__first-part__text">
        Ready to take your online presence to the next level? Contact us today for a free consultation. Let's turn your vision into a digital reality that captivates and converts.
      </div>
    </div>
    <div class="contact-form__second-part">
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
        <path
          d="M80.6087 403.043V537.391H0V403.043H80.6087Z"
          fill="white"
        />
      </svg>
    </div>
  </div>
</template>

<script setup>
  import {ref} from 'vue';
  const formData = ref({
    name: '',
    email: '',
  });
  const emits = defineEmits(['submit']);

  const handleSendForm = () => {
    emits('submit', formData.value);
  };
</script>

<style scoped lang="scss">
  .contact-form {
    display: flex;
    flex-direction: row;
    width: 100%;
    align-items: center;
    justify-content: space-between;

    &__first-part {
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      height: 100%;
      gap: 50px;

      &__text {
        font-size: 32px;
        font-family: var(--font-futura-regular);
        color: #ababab;
        width: 85%;

        @include w-max($sm) {
          font-size: 20px;
          text-align: center;
        }
      }

      &__form {
        display: flex;
        flex-direction: column;
        padding: 20px 60px;
        border: 1px solid #939393;
        border-radius: 20px;
        align-items: center;
        justify-content: center;
        gap: 20px;
        width: 85%;

        &__header {
          font-family: var(--font-futura-bold);
          font-size: 48px;
          color: white;

          @include w-max($sm) {
            font-size: 24px;
            text-align: center;
          }
        }

        input {
          border: 1px solid #939393;
          border-radius: 20px;
          padding: 10px;
          color: #939393;
          font-size: 16px;
          background-color: transparent;
          width: 100%;

          @include w-max($sm) {
            width: 120%;
            font-size: 16px;
          }
        }

        &__submit {
          color: black;
          background-color: white;
          padding: 10px 40px;
          font-family: var(--font-futura-bold);
          border-radius: 20px;
          transition: all 0.3s ease;

          @include w-max($sm) {
            font-size: 16px;
          }

          &:hover {
            cursor: pointer;
            background-color: rgb(187, 187, 187);
          }
        }
      }
    }

    &__second-part {
      @include w-max($md) {
        display: none;
      }
    }
  }
</style>
