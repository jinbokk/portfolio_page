<template>
  <section class="section_3">
    <carousel @nextPage="nextPage" @prevPage="prevPage">
      <carousel-slide
        v-for="(slide, index) in slides"
        :key="slide"
        :index="index"
        :visibleSlide="visibleSlide"
        :direction="direction"
      >
        <img :src="slide" />
      </carousel-slide>
    </carousel>
  </section>
</template>

<script>
import Carousel from "../components/Carousel.vue";
import CarouselSlide from "../components/CarouselSlide.vue";

export default {
  data() {
    return {
      slides: [
        require("../assets/portfolio_musicor.png"),
        require("../assets/portfolio_netflix.png"),
        require("../assets/portfolio_jinbokNews.png"),
      ],
      visibleSlide: 0,
      direction: "",
    };
  },

  components: {
    Carousel,
    CarouselSlide,
  },

  methods: {
    prevPage() {
      if (this.visibleSlide <= 0) {
        this.visibleSlide >= this.slides.length - 1;
      } else {
        this.visibleSlide--;
      }
      this.direction = "right";
    },

    nextPage() {
      if (this.visibleSlide >= this.slides.length - 1) {
        this.visibleSlideSlide = 0;
      } else {
        this.visibleSlide++;
      }
      this.direction = "left";
    },
  },
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

.section_3 img {
  height: 100vh;
  transform: scale(0.85);
}

.section_3_text_container {
  width: 100vw;
  height: 100vh;
}
</style>
