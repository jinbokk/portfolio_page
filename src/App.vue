<template>
  <div>
    <nav-bar></nav-bar>
    <section-1></section-1>
    <section-2></section-2>
    <section-3></section-3>
    <!-- <section-4></section-4> -->
    <!-- <section-5></section-5> -->
  </div>
</template>

<script>
import NavBar from "./components/NavBar.vue";
import Section1 from "./components/Section1.vue";
import Section2 from "./components/Section2.vue";
import Section3 from "./components/Section3.vue";
import Section4 from "./components/Section4.vue";
import Section5 from "./components/Section5.vue";

export default {
  name: "App",

  components: {
    NavBar,
    Section1,
    Section2,
    Section3,
    Section4,
    Section5,
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
}
</style>
