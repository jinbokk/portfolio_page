<!-- eslint-disable vue/multi-word-component-names -->
<template>
  <section class="section_2">
    <div class="section_2_img_container">
      <img :src="profile_img" />
    </div>
    <div class="section_2_text_container">
      <h2 class="section_2_about">ABOUT</h2>
      <h3 class="section_2_title"></h3>
      <p>내용쓰기내용쓰기내용쓰기내용쓰기내용쓰기내용쓰기내용쓰기내용쓰기</p>
    </div>
  </section>
</template>

<script>
export default {
  data() {
    return {
      profile_img: require("../assets/section_2_img.jpg"),
    };
  },
};
</script>

<style>
.section_2 {
  position: absolute;
  top: 100vh;
  height: 100vh;
  width: 100vw;
  background-color: rgb(15, 25, 34);
  display: flex;
  overflow: hidden;
}

.section_2_img_container {
  width: 50vw;
}

.section_2 img {
  position: absolute;
  bottom: 0;
  max-width: 50vw;
  min-height: 100vh;
  object-fit: cover;
}

.section_2_text_container {
  display: flex;
  flex-direction: column;
  justify-content: center;
  padding-left: 5rem;
}
</style>
