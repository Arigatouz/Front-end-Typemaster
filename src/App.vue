<template>
  <Navigation />
  <header-component></header-component>
  <main-section></main-section>
  <features-section></features-section>
  <footer-section></footer-section>
</template>

<script>
/* eslint-disable */
import Navigation from "./components/Navigation";
import HeaderComponent from "./components/HeaderComponent.vue";
import MainSection from "./components/MainSection";
import FeaturesSection from "./components/FeaturesSection";
import FooterSection from "./components/FooterSection.vue";
export default {
  name: "App",
  components: {
    Navigation,
    HeaderComponent,
    MainSection,
    FeaturesSection,
    FooterSection,
  },
};
</script>

<style lang="scss">
@import "./assets/scss/style.scss";
@import url("https://fonts.googleapis.com/css2?family=Barlow:ital,wght@0,100;0,400;0,900;1,100&display=swap");

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
  max-width: 1440px;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  margin-top: 3rem;
}
</style>
