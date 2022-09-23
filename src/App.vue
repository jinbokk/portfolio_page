<template>
  <nav-bar></nav-bar>
  <side-bar></side-bar>
  <landing-page class="scroll_element" id="landing_page"></landing-page>
  <about-page class="scroll_element" id="about_page"></about-page>
  <carousel-page class="scroll_element" id="carousel_page"></carousel-page>
  <contact-page class="scroll_element" id="contact_page"></contact-page>
</template>

<script>
import NavBar from "./components/NavBar.vue";
import SideBar from "./components/SideBar.vue";
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
    SideBar,
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
  background-color: rgb(11, 25, 47);
  height: 100vh;
  width: 100vw;
  margin: 0;
  padding: 0;
  overflow: hidden;
  user-select: none;
}

.scroll_container {
  height: 100%;
  overflow: auto;
  scroll-snap-type: y mandatory;
  -ms-overflow-style: none;
  scrollbar-width: none;
}

.scroll_container::-webkit-scrollbar {
  display: none;
}

.scroll_element {
  scroll-snap-align: start;
}
</style>
