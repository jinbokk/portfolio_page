<template>
  <div class="about_page_container_top" ref="about_page_container_top">
    <div class="about_page_container">
      <div class="about_page_img_container">
        <img :src="profile_img" />
      </div>
      <div class="about_page_text_container">
        <h2 class="about_page_about">ABOUT</h2>
        <h3 class="about_page_title"></h3>
        <p>안녕하세요 이진복 입니다</p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      profile_img: require("../assets/about_page_img.jpg"),
    };
  },

  methods: {
    sendData() {
      this.$emit("send_data");
    },
  },
};
</script>
y

<style>
.about_page_container_top {
  display: flex;
  justify-content: center;
  width: 100vw;
}

.about_page_container {
  height: 100vh;
  width: 85vw;
  background-color: rgb(15, 25, 34);
  display: flex;
}

.about_page_img_container {
  width: 40vw;
  overflow: hidden;
}

.about_page_img_container img {
  position: relative;
  max-width: 50vw;
  min-height: 100vh;
  object-fit: cover;
}

.about_page_text_container {
  display: flex;
  flex-direction: column;
  justify-content: center;
  padding-left: 5rem;
}
</style>
