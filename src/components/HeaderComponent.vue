<template>
  <!--eslint-disable -->
  <header class="header">
    <div class="header__container">
      <img
        class="header__pattern"
        src="../assets/shared/pattern-square.svg"
        alt=""
      />
      <div class="header__info">
        <div class="header__info__title">
          <h1>TypeMaster Keyboard</h1>
        </div>
        <div class="header__info__body">
          Improve your productivity and gaming without breaking the bank.
          Upgrade to a high quality mechanical typing experience.
        </div>
        <div class="header__info__action">
          <button class="header__info__action__btn">Pre-order now</button>
          <div class="header__info__action__date"><p>Release on 5/27</p></div>
        </div>
      </div>
      <div class="header__imageBox">
        <picture>
          <source
            srcset="
              ../assets/mobile/image-keyboard.jpg   950w,
              ../assets/tablet/image-keyboard.jpg  1279w,
              ../assets/desktop/image-keyboard.jpg 1640w
            "
          />
          <img
            class="header__imageBox__image"
            src="../assets/mobile/image-keyboard.jpg"
            alt="keyboard image"
          />
        </picture>
      </div>
    </div>
  </header>
</template>
<script>
/*eslint-disable */
export default {
  name: "Header",
};
</script>
<style lang="scss" scoped>
@import "../assets/scss/style.scss";
@import url("https://fonts.googleapis.com/css2?family=Barlow:wght@900&display=swap");
.header {
  margin-top: 6rem;
  width: 100%;
  position: relative;
  overflow: hidden;

  @include respond(tab) {
    margin-bottom: 5rem;
  }
  &__pattern {
    display: none;
    @include respond(deskTop) {
      display: inline-block;
      position: absolute;
      right: -17rem;
    }
  }
  &__container {
    margin-bottom: 3rem;
    @include respond(tab) {
      display: flex;
      margin-left: 5rem;
    }
    @include respond(deskTop) {
      justify-content: center;
    }
  }
  &__info {
    width: 32.4rem;
    margin: 0 auto;
    @include respond(tab) {
      width: 43.9rem;
      margin-top: 5rem;
    }
    @include respond(deskTop) {
      width: 50%;
      margin-left: 10rem;
    }

    &__title {
      font-family: "Barlow", sans-serif;
      margin: 0 0 2rem -1rem;
      font-size: 2.5rem;
      text-transform: uppercase;
      line-height: 1.1;
      color: var(--Header-color);
      @include respond(tab) {
        font-size: 2.8rem;
      }
      @include respond(deskTop) {
        font-size: 5rem;
      }
    }
    &__body {
      font-size: 1.65rem;
      color: var(--body-color);
      line-height: 1.5;
      margin-bottom: 2rem;
      @include respond(tab) {
        margin-bottom: 4rem;
      }
      @include respond(deskTop) {
        font-size: 1.8rem;
        width: 40rem;
      }
    }
    &__action {
      display: flex;
      margin-bottom: 6rem;
      align-items: center;
      &__btn {
        cursor: pointer;
        text-align: center;
        border: none;
        font-family: var(--font-Barlow);
        background-color: var(--main-color);
        color: var(--white);
        font-size: 1.6rem;
        padding: 1.3rem 2.3rem;
        text-transform: uppercase;
        border-radius: 0.7rem;
        box-shadow: 0 0.1rem 0.1rem rgba(0, 0, 0, 0.5);
        transition: all 0.4s ease-out;
        background-image: linear-gradient(
          150deg,
          transparent 0%,
          transparent 50%,
          var(--main-color-hover) 50%
        );
        background-size: 240%;
        @include respond(tab) {
          padding: 1.9rem 2.8rem;
          font-size: 1.6rem;
          background-image: linear-gradient(
            130deg,
            transparent 0%,
            transparent 50%,
            var(--main-color-hover) 50%
          );
        }
        &:hover,
        &:focus {
          background-position: 100%;
        }
      }
      &__date {
        margin-left: 3rem;
        & p {
          font-size: 1.6rem;
          color: var(--body-color);
          cursor: context-menu;
          transition: all 0.3s ease;
          transform: scale(1);
          position: relative;
          @include respond(tab) {
          }
          &::after {
            content: "";
            position: absolute;
            bottom: -1rem;
            left: 0;
            width: 10rem;
            height: 3px;
            background-color: var(--main-color-hover);
            display: none;
            @include respond(tab) {
              width: 12rem;
            }
          }
          &:hover {
            color: var(--main-color-hover);
            font-weight: 900;
            transform: scale(1.2);
            &::after {
              display: block;
            }
          }
        }
      }
    }
  }
  &__imageBox {
    overflow: hidden;
    margin-left: 3rem;
    @include respond(deskTop) {
      width: 52%;
    }
    &__image {
      border-radius: 2rem;
      width: 37.2rem;
      height: 33.1rem;
      @include respond(tab) {
        margin-left: 1rem;
        width: 47.8rem;
        height: 42.5rem;
        border-radius: 3rem;
      }
      @include respond(deskTop) {
        width: 54rem;
        height: 48rem;
      }
    }
    @include respond(deskTop) {
      margin-left: 0;
    }
  }
}
</style>
