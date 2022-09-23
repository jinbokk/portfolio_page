<template>
  <div class="landing_page_container_top">
    <div class="landing_page_container">
      <h1 class="landing_page_title">With<br />Infinite<br />Potential</h1>
      <button class="landing_page_button" @click="handleClick">
        HELLO, JINBOK!
      </button>
    </div>
  </div>
</template>

<script>
export default {
  mounted() {
    const scrollElement = document.getElementById("landing_page");
    window.addEventListener("scroll", this.handleScroll(scrollElement));
  },

  methods: {
    handleScroll(e) {
      // const windowScrollY = window.scrollY;
      console.log(e);
      console.log(e.style); // something wrong !!!!!!!!!!!!!
    },

    handleClick() {
      console.log("clicked!");
      window.scroll({
        top: 100,
        behavior: "smooth",
      });
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
  text-shadow: rgb(94, 239, 206, 0.5) 8px 8px;
  pointer-events: none;
  user-select: none;
}

.landing_page_button {
  cursor: pointer;
  color: aliceblue;
  margin-top: 1rem;
  border: rgb(220, 220, 220) solid 1px;
  background-color: transparent;
  font-size: 1rem;
  font-weight: bold;
  padding: 1rem;
  width: 150px;
  box-shadow: inset 0 0 0 0 black;
  transition: color 0.3s ease-in-out, box-shadow 0.3s ease-in-out;
  user-select: none;
}

.landing_page_button:hover {
  box-shadow: inset 160px 0 0 0 rgb(94, 239, 206);
  color: black;
  border: rgb(220, 220, 220, 0.5) solid 1px;
}
</style>
