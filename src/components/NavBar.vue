<template>
  <div class="nav_container_top">
    <div class="nav_container">
      <a class="nav_logo">JINBOK LEE</a>
      <div class="nav_container_items">
        <div class="nav_container_menu">
          <a>ABOUT</a>
          <a>CONTACT</a>
        </div>
        <div class="nav_container_icon">
          <img src="../assets/github_icon.png" class="nav_icon" />
          <img
            src="../assets/velog_icon.png"
            class="nav_icon"
            style="margin-right: 0"
          />
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style>
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
  margin-right: 0.7rem;
}

.nav_container_icon img {
  margin-right: 0.7rem;
}

.nav_icon {
  width: 25px;
}
</style>
