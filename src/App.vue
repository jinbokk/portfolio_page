<template>
  <nav>
    <div class="nav_container_top">
      <div class="nav_container">
        <a class="nav_logo">JINBOK LEE</a>
        <div class="nav_container_items">
          <div class="nav_container_menu">
            <a>ABOUT</a>
            <a>CONTACT</a>
          </div>
          <div class="nav_container_icon">
            <img src="./assets/github_icon.png" class="nav_icon" />
            <img
              src="./assets/velog_icon.png"
              class="nav_icon"
              style="margin-right: 0"
            />
          </div>
        </div>
      </div>
    </div>
  </nav>

  <section class="section_1">
    <h1 class="section_1_title">With<br />Infinite<br />Potential</h1>
    <div><a class="section_1_button">HELLO, JINBOK!</a></div>
  </section>

  <section class="section_2">
    <div>
      <img
        src="./assets/section_2_img.jpg"
        style="max-width: 50vw; min-height: 100vh; object-fit: cover"
      />
    </div>
    <div class="section_2_text_section">
      <h2 class="section_2_about">ABOUT</h2>
      <h3 class="section_2_title"></h3>
      <p>내용쓰기내용쓰기내용쓰기내용쓰기내용쓰기내용쓰기내용쓰기내용쓰기</p>
    </div>
  </section>

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
import Carousel from "./components/Carousel.vue";
import CarouselSlide from "./components/CarouselSlide.vue";

export default {
  name: "App",

  data() {
    return {
      slides: [
        require("./assets/portfolio_musicor.png"),
        require("./assets/portfolio_netflix.png"),
        require("./assets/portfolio_jinbokNews.png"),
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
html,
body {
  color: rgb(220, 220, 220);
  background-color: rgb(40, 40, 40);
  height: 100vh;
  width: 100vw;
  margin: 0;
  padding: 0;
}

.nav_container_top {
  position: fixed;
  display: flex;
  justify-content: space-around;
  width: 100%;
  padding: 1rem 0;
  z-index: 100;
}

.nav_container {
  width: 80vw;
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.nav_logo {
  font-size: 1.2rem;
  font-weight: bold;
}

.nav_container_items {
  display: flex;
}

.nav_container_menu {
  display: flex;
  align-items: center;
}

.nav_container_menu a {
  display: flex;
  align-items: center;
  margin-right: 0.7rem;
}

.nav_container_icon img {
  margin-right: 0.7rem;
}

.nav_icon {
  width: 25px;
}

.section_1 {
  position: fixed;
  height: 100vh;
  width: 100vw;
  display: flex;
  flex-direction: column;
  justify-content: center;
  text-align: center;
  line-height: 1.5;
  font-weight: bold;
}

.section_1_title {
  font-size: 3rem;
}

.section_1_button {
  cursor: pointer;
  margin-top: 5rem;
  border: rgb(220, 220, 220) solid 1px;
  padding: 1rem;
  box-shadow: inset 0 0 0 0 #98369a;
  transition: color 0.3s ease-in-out, box-shadow 0.3s ease-in-out;
}

.section_1_button:hover {
  box-shadow: inset 130px 0 0 0 #98369a;
  color: white;
}

.section_2 {
  position: absolute;
  top: 100vh;
  height: 100vh;
  width: 100vw;
  background-color: rgb(15, 25, 34);
  display: flex;
  overflow: hidden;
}

.section_2_text_section {
  display: flex;
  flex-direction: column;
  justify-content: center;
  padding-left: 5rem;
}
</style>
