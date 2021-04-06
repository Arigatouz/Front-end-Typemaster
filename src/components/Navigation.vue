<template>
  <div class="navigation">
    <ul class="navigation__list">
      <li class="navigation__item">
        <img class="navigation__logo" src="../assets/shared/logo.svg" alt="" />
      </li>
      <li class="navigation__item">
        <button class="navigation__btn">Pre-order now</button>
      </li>
    </ul>
  </div>
</template>

<script>
/* eslint-disable */
export default {
  name: "Navigation",
};
</script>
<style scoped lang="scss">
@import "../assets/scss/style.scss";
.navigation {
  width: 90%;
  margin: 0 auto;
  &__list {
    width: 100%;
    display: flex;
    list-style-type: none;
    justify-content: space-around;
    align-items: center;
    @include respond(smallTab){
      justify-content: space-between;
    }
  }
  &__item {
    width: 50%;

    @include respond(smallTab){
      width: 32%;
    }
    @include respond(tab){
      width: 25%;
    }
  }
  &__logo {
    width: 4rem;
    height: 4rem;
  }
  &__btn {
    cursor: pointer;
    text-align: center;
    border: none;
    font-family: var(--font-Barlow);
    background-color: var(--gray-color);
    color: var(--Header-color);
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
      var(--Header-color) 50%
    );
    background-size: 240%;
    &:hover,
    &:focus {
      background-position: 100%;
      color: var(--white);
    }
  }
}
</style>
