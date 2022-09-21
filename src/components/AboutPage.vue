<!-- eslint-disable vue/multi-word-component-names -->
<template>
  <div class="about_page">
    <div class="about_page_img_container">
      <img :src="profile_img" />
    </div>
    <div class="about_page_text_container">
      <h2 class="about_page_about">ABOUT</h2>
      <h3 class="about_page_title"></h3>
      <p>내용쓰기내용쓰기내용쓰기내용쓰기내용쓰기내용쓰기내용쓰기내용쓰기</p>
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
};
</script>
y

<style>
.about_page {
  position: absolute;
  top: 100vh;
  height: 100vh;
  width: 100vw;
  background-color: rgb(15, 25, 34);
  display: flex;
  overflow: hidden;
}

.about_page_img_container {
  width: 50vw;
}

.about_page img {
  position: absolute;
  bottom: 0;
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
