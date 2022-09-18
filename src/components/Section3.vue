<template>
  <section class="section_3">
    <swiper
      :modules="modules"
      effect="fade"
      :slides-per-view="1"
      :space-between="0"
      navigation
      :pagination="{ clickable: true }"
      :loop="true"
      :autoplay="false"
      :speed="500"
    >
      <swiper-slide
        v-for="(slide, index) in slides"
        :key="slide"
        :index="index"
      >
        <img :src="slide" />
      </swiper-slide>
    </swiper>
  </section>
</template>

<script>
import { Navigation, Pagination, Scrollbar, A11y, Autoplay } from "swiper";
import { Swiper, SwiperSlide } from "swiper/vue";
import { EffectFade } from "swiper";

import "swiper/css";
import "swiper/css/navigation";
import "swiper/css/pagination";
import "swiper/css/effect-fade";

export default {
  components: {
    Swiper,
    SwiperSlide,
  },

  setup() {
    return {
      slides: [
        require("../assets/portfolio_musicor.png"),
        require("../assets/portfolio_netflix.png"),
        require("../assets/portfolio_jinbokNews.png"),
      ],
      modules: [Navigation, Pagination, Scrollbar, A11y, EffectFade, Autoplay],
    };
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

.swiper-slide {
  display: flex;
  justify-content: center;
}

.section_3 img {
  height: 100vh;
  transform: scale(0.85);
  pointer-events: none;
  user-select: none;
}

.section_3_text_container {
  width: 100vw;
  height: 100vh;
}
</style>
