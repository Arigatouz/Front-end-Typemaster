<template>
  <!-- eslint-disable  -->
  <main class="main">
    <div class="main__container">
      <img
        class="main__container__pattern"
        src="../assets/shared/pattern-square.svg"
        alt=""
      />
      <div class="main__box">
        <div class="main__box__image1">
          <div class="main__box__overlay"></div>
          <picture>
            <source
              srcset="
                ../assets/mobile/image-phone-and-keyboard.jpg   950w,
                ../assets/tablet/image-phone-and-keyboard.jpg  1297w,
                ../assets/desktop/image-phone-and-keyboard.jpg 1640w
              "
            />
            <img
              src="../assets/mobile/image-phone-and-keyboard.jpg"
              alt="keyboard image 1"
            />
          </picture>
        </div>
        <div class="main__box__image2">
          <picture>
            <source
              srcset="
                ../assets/mobile/image-glass-and-keyboard.jpg   950w,
                ../assets/tablet/image-glass-and-keyboard.jpg  1297w,
                ../assets/desktop/image-glass-and-keyboard.jpg 1640w
              "
            />
            <img
              src="../assets/mobile/image-phone-and-keyboard.jpg"
              alt="keyboard image 1"
            />
          </picture>
        </div>
      </div>
      <div class="main__info">
        <h2 class="main__info__title">mechanical wireless Keyboard</h2>
        <p class="main__info__body">
          The Typemaster keyboard boasts top-notch build and practical design.
          It offers a wide variety of switches and keycaps, along with reliable
          wireless connectivity.
        </p>
      </div>
    </div>
  </main>
</template>
<script>
/*eslint-disable */
export default {
  name: "main-section",
};
</script>
<style lang="scss" scoped>
@import "../assets/scss/style.scss";
.main {
  &__container {
    @include respond(deskTop) {
      display: flex;
      position: relative;
    }
    &__pattern {
      display: none;
      @include respond(deskTop) {
        display: inline-block;
        position: absolute;
        bottom: 6rem;
        left: -15rem;
      }
    }
  }
  &__box {
    display: flex;
    margin-bottom: 6rem;
    @include respond(tab) {
      justify-content: center;
    }
    @include respond(deskTop) {
      margin-left: 15rem;
    }
    &__overlay {
      width: 12.9rem;
      height: 19.3rem;
      background-color: #f84108;
      position: absolute;
      opacity: 0.5;
      margin-left: -2rem;
      border-radius: 2rem;
      @include respond(tab) {
        width: 21.4rem;
        height: 32rem;
        margin-left: 0;
      }
      @include respond(deskTop) {
        width: 25.5rem;
        height: 48rem;
      }
    }
    &__image1 {
      & picture {
        & img {
          margin-left: -2rem;
          width: 12.9rem;
          height: 19.3rem;
          border-radius: 2rem;
          @include respond(tab) {
            width: 21.4rem;
            height: 32rem;
            margin-left: 0;
          }
          @include respond(deskTop) {
            width: 25.5rem;
            height: 48rem;
          }
        }
      }
    }
    &__image2 {
      & picture {
        & img {
          margin-left: 3rem;
          width: 22rem;
          height: 19.3rem;
          border-radius: 2rem;
          @include respond(tab) {
            width: 44.5rem;
            height: 32rem;
          }
          @include respond(deskTop) {
            height: 48rem;
          }
        }
      }
    }
  }
  &__info {
    width: 32.7rem;
    margin: 0 auto;
    @include respond(tab) {
      width: 90%;
      display: flex;
      justify-content: space-around;
    }
    @include respond(deskTop) {
      display: block;
      margin-top: 8rem;
      width: 25.5rem;
      height: 26rem;
    }
    &__title {
      font-size: 3.9rem;
      text-transform: uppercase;
      font-weight: 500;
      text-align: center;
      margin-bottom: 2rem;
      @include respond(tab) {
        font-size: 3.2rem;
        text-align: left;
        margin-right: 8rem;
      }
    }
    &__body {
      text-align: center;
      font-size: 1.65rem;
      color: var(--body-color);
      line-height: 1.5;
      margin-bottom: 2rem;
      @include respond(tab) {
        font-size: 1.7rem;
        line-height: 1.8;
        align-self: center;
        text-align: left;
      }
    }
  }
}
</style>
