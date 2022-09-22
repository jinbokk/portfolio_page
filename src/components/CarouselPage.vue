<template>
  <div class="carousel_page_container_top">

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
.carousel_page_container_top {
  height: 100vh;
  width: 100vw;
  background-color: brown;
}
</style>
