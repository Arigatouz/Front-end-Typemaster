<template>
  <Navigation />
  <header-component></header-component>
  <main-section></main-section>
</template>

<script>
/* eslint-disable */
import Navigation from "./components/Navigation";
import HeaderComponent from "./components/HeaderComponent.vue";
import MainSection from "./components/MainSection";
export default {
  name: "App",
  components: {
    Navigation,
    HeaderComponent,
    MainSection,
  },
};
</script>

<style lang="scss">
@import url("https://fonts.googleapis.com/css2?family=Barlow:ital,wght@0,100;0,400;0,900;1,100&display=swap");

/* //break Points */
@mixin respond($breakpoint) {
  @if ($breakpoint == smallTab) {
    @media screen and (min-width: 700px) {
      @content;
    }
  }
  @if ($breakpoint == tab) {
    @media screen and (min-width: 900px) {
      @content;
    }
  }
  @if ($breakpoint == deskTop) {
    @media screen and (min-width: 1440px) {
      @content;
    }
  }
}

/* // general reset */
*,
*::before,
*::after {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
html {
  font-size: 62.5%;
  font-family: var(--font-Barlow);
}

:root {
  /* // Color declaration */
  --main-color: #f16718;
  --main-color-hover: #ff9b62;
  --Header-color: #162542;
  --body-color: #7b8bad;
  --gray-color: #e8eff2;
  --white: #fff;
  /* // font declaration */
  // font-family: "Barlow", sans-serif;
  --font-Barlow: "Barlow", sans-serif;
}
#app {
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  margin-top: 3rem;
}
</style>
