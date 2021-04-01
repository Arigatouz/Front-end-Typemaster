<template>
  <!--eslint-disable -->
  <header class="header">
    <div class="header__container">
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
.header {
  margin-top: 6rem;
  &__container {
    margin-bottom: 3rem;
  }
  &__info {
    width: 32.4rem;
    margin: 0 auto;
    &__title {
      margin: 0 0 2rem -1rem;
      font-size: 2.5rem;
      font-style: oblique;
      text-transform: uppercase;
      line-height: 1.1;
      color: var(--Header-color);
    }
    &__body {
      font-size: 1.65rem;
      color: var(--body-color);
      line-height: 1.5;
      margin-bottom: 2rem;
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
        &:hover,
        &:focus {
          background-position: 100%;
        }
      }
      &__date {
        margin-left: 3rem;
        & p {
          font-size: 1.3rem;
          color: var(--body-color);
          cursor: context-menu;
          transition: all 0.3s ease;
          transform: scale(1);
          position: relative;
          &::after {
            content: "";
            position: absolute;
            bottom: -1rem;
            left: 0;
            width: 10rem;
            height: 3px;
            background-color: var(--main-color-hover);
            display: none;
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
    &__image {
      border-radius: 2rem;
      width: 37.2rem;
      height: 33.1rem;
    }
  }
}
</style>
