<!-- eslint-disable vue/multi-word-component-names -->
<template>
  <div class="carousel_page">
    <v-carousel height="100vh" width="100vw" cycle show-arrows-on-hover>

          <v-carousel-item
            v-for="(slide, index) in slides"
            :key="index"
            :src="slide"
            :disabled="true"
            reverse-transition="fade-transition"
            transition="fade-transition"
          ></v-carousel-item>

    </v-carousel>
  </div>
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
.carousel_page {
  position: relative;
  top: 200vh;
  height: 100vh;
  width: 100vw;
  background-color: brown;
  /* white-space: nowrap; */
}
</style>
