<template>
  <div class="carousel_page_container_top">
    <font-awesome-icon
      class="carousel_button"
      @click="handleSlideButtonPrev"
      icon="fa-solid fa-circle-chevron-left"
    />
    <div class="carousel_container">
      <div class="carousel_item_container">
        <div v-for="(slide, index) in slides" :key="index">
            <img
              class="carousel_item"
              :src="slide"
              :current-slide="currentSlide"
              v-show="currentSlide === index"
            />
        </div>
      </div>
      <div class="carousel_indicator_container">
        <button
          v-for="(slide, index) in slides"
          :key="index"
          class="carousel_indicator"
          :class="{ active: currentSlide === index }"
          @click="handleSlideIndicator"
        ></button>
      </div>
    </div>
    <font-awesome-icon
      class="carousel_button"
      @click="handleSlideButtonNext"
      icon="fa-solid fa-circle-chevron-right"
    />
  </div>
</template>

<script>
export default {
  data: () => ({
    model: 0,
    slides: [
      require("../assets/portfolio_netflix.png"),
      require("../assets/portfolio_musicor.png"),
      require("../assets/portfolio_jinbokNews.png"),
    ],
    currentSlide: 0,
  }),
  methods: {
    handleSlideButtonPrev() {
      if (this.currentSlide === 0) {
        return;
      } else if (this.currentSlide < this.slides.length) {
        this.currentSlide = this.currentSlide - 1;
      }
    },

    handleSlideButtonNext() {
      if (this.currentSlide < this.slides.length - 1) {
        this.currentSlide = this.currentSlide + 1;
      } else if (this.currentSlide === this.slides.length - 1) {
        console.log(this.currentSlide);
        return;
      }
    },

    handleSlideIndicator() {},
  },
};
</script>

<style>
.carousel_page_container_top {
  height: 100vh;
  width: 100vw;
  display: flex;
  justify-content: center;
  align-items: center;
  overflow: hidden;
}

.carousel_container {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  overflow: hidden;
}

.carousel_item_container {
  display: flex;
  justify-content: center;
  align-items: center;
  user-select: none;
  pointer-events: none;
}

.carousel_item {
  height: 80vh;
  width: 80vw;
  object-fit: contain;
  user-select: none;
  pointer-events: none;
}

.carousel_button {
  height: 40px;
  width: 40px;
  padding: 10px;
  position: relative;
  cursor: pointer;
  opacity: 0.5;
  transition: 0.3s;
}

.carousel_button:hover {
  opacity: 1;
  transition: 0.3s;
}

.carousel_indicator_container {
  display: flex;
  justify-content: center;
  align-items: center;
}

.carousel_indicator {
  width: 15px;
  height: 15px;
  margin: 0 10px;
  border-radius: 50%;
  cursor: pointer;
  transition: 0.3s;
  border: none;
  background-color: rgb(255, 255, 255, 0.5);
}

.active {
  background-color: rgb(255, 255, 255);
}

.carousel_indicator:hover {
  transform: scale(1.2);
  transition: 0.3s;
  background-color: rgb(255, 255, 255);
}

.carousel_indicator:active {
  transform: scale(1);
}

</style>
