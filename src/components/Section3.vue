<!-- eslint-disable vue/multi-word-component-names -->
<template>
  <section class="section_3">
    <v-carousel height="100%">
      <!-- <v-row class="fill-height" align="center" justify="center"> -->
      <v-carousel-item
        v-for="(slide, index) in slides"
        :key="index"
        :src="slide"
        :disabled="true"
        reverse-transition="fade-transition"
        transition="fade-transition"
        class="v-carousel_item"
      ></v-carousel-item>
      <!-- </v-row> -->
    </v-carousel>
  </section>
</template>

<script>
export default {
  data: () => ({
    model: 0,
    slides: [
      require("../assets/portfolio_musicor.png"),
      require("../assets/portfolio_netflix.png"),
      require("../assets/portfolio_jinbokNews.png"),
    ],
  }),
};
</script>

<style>
.section_3 {
  position: absolute;
  top: 200vh;
  height: 100vh;
  width: 100vw;
  background-color: brown;
  white-space: nowrap;
}

.v-carousel_item {
  height: 200px;
  pointer-events: none;
  user-select: none;
}
</style>
