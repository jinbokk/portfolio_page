<template>
  <div @scroll="handleScroll">
    <nav-bar></nav-bar>
    <landing-page></landing-page>
    <about-page></about-page>
    <carousel-page></carousel-page>
    <contact-page></contact-page>
  </div>
</template>

<script>
import NavBar from "./components/NavBar.vue";
import LandingPage from "./components/LandingPage.vue";
import AboutPage from "./components/AboutPage.vue";
import CarouselPage from "./components/CarouselPage.vue";
import ContactPage from "./components/ContactPage.vue";

export default {
  name: "App",

  components: {
    NavBar,
    LandingPage,
    AboutPage,
    CarouselPage,
    ContactPage,
  },

  methods: {
    handleScroll(e) {
      console.log("scroll fired", e);
    },
  },
};
</script>

<style>
html,
body {
  color: rgb(220, 220, 220);
  background-color: rgb(40, 40, 40);
  height: 100vh;
  width: 100vw;
  margin: 0;
  padding: 0;
  /* display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center; */
}
</style>
