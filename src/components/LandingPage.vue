<template>
  <div class="landing_page_container_top">
    <div class="landing_page_container" ref="landing_page_container">
      <h1 class="landing_page_title">With<br />Infinite<br />Potential</h1>
      <div class="landing_page_button">HELLO, JINBOK!</div>
    </div>
  </div>
</template>

<script>
export default {
  data() {},

  mounted() {
    const landing_page_container = this.$refs.landing_page_container;
    window.addEventListener(
      "scroll",
      this.handleScroll(landing_page_container)
    );
  },

  methods: {
    handleScroll(e) {
      // const windowScrollY = window.scrollY;
      console.log(e.style);
      // e.style.backgroundColor = "red";
    },
  },
};
</script>

<style>
.landing_page_container_top {
  height: 100vh;
  width: 100vw;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  text-align: center;
  line-height: 1.5;
  font-weight: bold;
  background-color: rgb(55, 55, 55);
}

.landing_page_container {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}

.landing_page_title {
  font-size: 7rem;
  font-weight: bold;
  color: aliceblue;
  text-shadow: rgb(30, 30, 30) 12px 10px;
}

.landing_page_button {
  cursor: pointer;
  color: aliceblue;
  margin-top: 1rem;
  border: rgb(220, 220, 220) solid 1px;
  padding: 1rem;
  width: 120px;
  box-shadow: inset 0 0 0 0 black;
  transition: color 0.3s ease-in-out, box-shadow 0.3s ease-in-out;
  text-shadow: rgb(30, 30, 30) 3px 3px;
}

.landing_page_button:hover {
  box-shadow: inset 150px 0 0 0 black;
  color: white;
}
</style>
