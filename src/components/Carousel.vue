<template>
  <div>
    <div class="section_3_pageButton_top">
      <div class="section_3_pageButton_container">
        <button @click="prevPage">LEFT</button>
        <button @click="nextPage">RIGHT</button>
      </div>
    </div>
    <div class="section_3_items">
      <slot></slot>
    </div>
    <div class="section_3_text_container">
      내용쓰기내용쓰기내용쓰기내용쓰기내용쓰기내용쓰기내용쓰기내용쓰기
      내용쓰기내용쓰기내용쓰기내용쓰기내용쓰기내용쓰기내용쓰기내용쓰기
      내용쓰기내용쓰기내용쓰기내용쓰기내용쓰기내용쓰기내용쓰기내용쓰기
      내용쓰기내용쓰기내용쓰기내용쓰기내용쓰기내용쓰기내용쓰기내용쓰기
      내용쓰기내용쓰기내용쓰기내용쓰기내용쓰기내용쓰기내용쓰기내용쓰기
      내용쓰기내용쓰기내용쓰기내용쓰기내용쓰기내용쓰기내용쓰기내용쓰기
      내용쓰기내용쓰기내용쓰기내용쓰기내용쓰기내용쓰기내용쓰기내용쓰기
      내용쓰기내용쓰기내용쓰기내용쓰기내용쓰기내용쓰기내용쓰기내용쓰기
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {};
  },
  methods: {
    prevPage() {
      this.$emit("prevPage");
    },

    nextPage() {
      this.$emit("nextPage");
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
  display: flex;
  overflow: hidden;
}

.section_3_pageButton_top {
  position: absolute;
  left: 5%;
}

.section_3_pageButton_container {
  position: absolute;
  top: 50vh;
  display: flex;
  width: 90vw;
  justify-content: space-between;
}

.section_3 img {
  height: 100vh;
  transform: scale(0.85);
}

.section_3_items {
  float: left;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  min-width: 100vw;
}

.section_3_text_container {
  width: 100vw;
  height: 100vh;
}
</style>
