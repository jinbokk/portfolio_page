<template>
  <nav-bar></nav-bar>
  <section-1></section-1>
  <section-2></section-2>
  <section-3></section-3>
</template>

<script>
import NavBar from "./components/NavBar.vue";
import Section1 from "./components/Section1.vue";
import Section2 from "./components/Section2.vue";
import Section3 from "./components/Section3.vue";

export default {
  name: "App",

  components: {
    NavBar,
    Section1,
    Section2,
    Section3,
  }
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
