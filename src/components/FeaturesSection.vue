<template>
  <!-- eslint-disable -->
  <section class="features">
    <div class="features__container">
      <div class="features__compatible">
        <div class="features__imageContainer">
          <img
            src="../assets/shared/icon-compatible.svg"
            alt="compatible Icon"
            class="features__icon"
          />
        </div>
        <h3 class="features__title">
          HIGHLY <br />
          COMPATIBLE
        </h3>
        <p class="features__info">
          Easy to use and works well with all major computer brands, gaming
          consoles and mobile devices. Plug & play, no installation or driver
          needed.
        </p>
      </div>
      <div class="features__wireless">
        <div class="features__imageContainer">
          <img
            src="../assets/shared/icon-bluetooth.svg"
            alt="bluetooth icon"
            class="features__icon"
          />
        </div>
        <h3 class="features__title">
          WIRELESS <br />
          WITH BLUETOOTH
        </h3>
        <p class="features__info">
          Powerful 2.4G RF technology allows you to connect the cordless
          keyboard from up to 30ft away. Simply plug the unifying receiver into
          your computer.
        </p>
      </div>
      <div class="features__battery">
        <div class="features__imageContainer">
          <img
            src="../assets/shared/icon-battery.svg"
            alt="battery icon"
            class="features__icon"
          />
        </div>
        <h3 class="features__title">
          HIGH CAPACITY <br />
          BATTERY
        </h3>
        <p class="features__info">
          Equipped with a long-lasting built-in battery, you’ll never have to
          spend a dime on replaceable ones. Enjoy 40 hours of usage time between
          charges.
        </p>
      </div>
      <div class="features__RGB">
        <div class="features__imageContainer">
          <img
            src="../assets/shared/icon-light.svg"
            alt="rgb backlit icon"
            class="features__icon"
          />
        </div>
        <h3 class="features__title">
          RGB BACKLIT <br />
          MODES
        </h3>
        <p class="features__info">
          Choose from 4 backlight brightness levels and adjustable breathing
          speed. Each key glows intensely in the dark and helps you type in low
          light conditions.
        </p>
      </div>
    </div>
  </section>
</template>
<script>
export default {
  /*eslint-disable */
  name: "features-section",
};
</script>

<style lang="scss" scoped>
@import "../assets/scss/style.scss";
.features {
  margin-top: 11.6rem;
  &__container {
    width: 32.7rem;
    margin: 0 auto;
    @include respond(tab) {
      width: 90%;
      display: grid;
      grid-template-columns: 1fr 1fr;
      grid-template-rows: 1fr 1fr;
      gap: 0px 0px;
      grid-auto-flow: row;
      grid-template-areas:
        ". ."
        ". .";
    }
  }
  &__compatible,
  &__wireless,
  &__battery,
  &__RGB {
    text-align: center;
    margin-bottom: 7rem;
    @include respond(tab){
      text-align: left;
    }
  }
  &__imageContainer {
    width: 6.5rem;
    height: 6.5rem;
    margin: 0 0 5rem 13rem;
    background-color: var(--main-color);
    border-radius: 1rem;
    display: flex;
    justify-content: center;
     @include respond(tab){
    margin-left: 0;
      
    }
  }
  &__icon {
    align-self: center;
    justify-self: center;
   
  }
  &__title {
    font-size: 2.4rem;
    font-weight: 400;
    margin-bottom: 3rem;
    color: var(--Header-color);
  }
  &__info {
    font-size: 1.6rem;
    color: var(--body-color);
    line-height: 1.6;
  }
}
</style>
