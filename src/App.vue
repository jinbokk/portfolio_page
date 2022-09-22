<template>
  <nav-bar></nav-bar>
  <landing-page class="scroll_element"></landing-page>
  <about-page class="scroll_element"></about-page>
  <carousel-page class="scroll_element"></carousel-page>
  <contact-page class="scroll_element"></contact-page>
</template>

<script>
import NavBar from "./components/NavBar.vue";
import LandingPage from "./components/LandingPage.vue";
import AboutPage from "./components/AboutPage.vue";
import CarouselPage from "./components/CarouselPage.vue";
import ContactPage from "./components/ContactPage.vue";

export default {
  mounted() {
    document.getElementById("app").classList.add("scroll_container");
  },

  components: {
    NavBar,
    LandingPage,
    AboutPage,
    CarouselPage,
    ContactPage,
  },
};
</script>

<style>
html,
body {
  color: rgb(220, 220, 220);
  background-color: rgb(29, 29, 29);
  height: 100vh;
  width: 100vw;
  margin: 0;
  padding: 0;
  overflow: hidden;
}

.scroll_container {
  height: 100%;
  overflow: auto;
  scroll-snap-type: y mandatory;
}

.scroll_element {
  scroll-snap-align: start;
}
</style>
