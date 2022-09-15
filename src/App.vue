<template>
  <nav>
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
  </nav>

  <section class="section_1">
    <h1 class="section_1_title">With<br />Infinite<br />Potential</h1>
    <div><a class="section_1_button">HELLO, JINBOK!</a></div>
  </section>
</template>

<script>
export default {
  name: "App",
  data() {
    return {
      //data 보관함
    };
  },
  components: {},
};
</script>

<style>
/* #App {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
} */

html,
body {
  color: rgb(220, 220, 220);
  background-color: rgb(40, 40, 40);
  height: 100vh;
  width: 100vw;
  margin: 0;
  padding: 0;
}

.nav_container {
  position: absolute;
  width: 100vw;
  display: flex;
  justify-content: space-between;
  align-items: center;
  /* padding: 0.8rem 2.5rem; */
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
  height: 100vh;
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
  margin-top: 5rem;
  border: rgb(220, 220, 220) solid 1px;
  padding: 1rem;
}
</style>
