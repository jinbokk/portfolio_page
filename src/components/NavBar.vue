<template>
  <div class="nav_container_top" :class="{ scrolled: handleScroll }">
    <div class="nav_container">
      <a class="nav_logo">JINBOK LEE</a>
      <div class="nav_container_items">
        <div class="nav_container_menu">
          <a>ABOUT</a>
          <a>CONTACT</a>
        </div>
        <div class="nav_container_icon">
          <img :src="github_icon" class="nav_icon" />
          <img :src="velog_icon" class="nav_icon" style="margin-right: 0" />
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      github_icon: require("../assets/github_icon.png"),
      velog_icon: require("../assets/velog_icon.png"),
      handleScroll: null,
    };
  },

  mounted() {
    window.addEventListener("scroll", this.updateScroll);
  },

  methods: {
    updateScroll() {
      const scrollPositionY = window.scrollY;
      if (scrollPositionY > window.innerHeight - 200) {
        this.handleScroll = true;
        return;
      } else if (scrollPositionY <= window.innerHeight - 200) {
        this.handleScroll = false;
      }
      this.scrollPositionY = false;
    },
  },
};
</script>

<style>
.nav_container_top {
  position: fixed;
  top: 0;
  display: flex;
  justify-content: space-around;
  width: 100%;
  padding: 1rem 0;
  z-index: 100;
  background: linear-gradient(to bottom, rgba(0, 0, 0, 0.7), transparent);
  transition: 0.5s;
}

.scrolled {
  background-color: rgb(25, 25, 25);
}

.nav_container {
  width: 80vw;
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.nav_logo {
  text-decoration: none;
  color: black;
  font-size: 1.2rem;
  font-weight: bold;
  color: aliceblue;
}

.nav_container_items {
  display: flex;
}

.nav_container_menu {
  display: flex;
  align-items: center;
  color: aliceblue;
  font-weight: bold;
}

.nav_container_menu a {
  display: flex;
  align-items: center;
  margin-right: 2rem;
}

.nav_container_icon img {
  margin-right: 1.2rem;
}

.nav_icon {
  width: 25px;
}
</style>
