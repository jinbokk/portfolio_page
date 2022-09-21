<!-- eslint-disable vue/multi-word-component-names -->
<template>
  <div>
    <div class="section_3_pageButton_top">
      <div class="section_3_pageButton_container">
        <button @click="prevPage">&#10094;</button>
        <button @click="nextPage">&#10095;</button>
      </div>
    </div>
    <div class="section_3_items">
      <slot></slot>
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
.section_3_pageButton_top {
  position: absolute;
  left: 5%;
  z-index: 10;
}

.section_3_pageButton_container {
  /* position: absolute;
  top: 50vh; */
  display: flex;
  width: 90vw;
  height: 100px;
  justify-content: space-between;
  align-items: center;
}

.section_3_pageButton_container button {
  background: blue;
  border: none;
  height: 100%;
  vertical-align: center;
  align-items: center;
  transform: scale(2);
}

.section_3_items {
  display: flex;
  flex-direction: row;
  align-items: center;
  justify-content: center;
  min-width: 100vw;
}
</style>
