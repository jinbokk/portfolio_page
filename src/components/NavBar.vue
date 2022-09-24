<template>
  <div class="nav_container_top" :class="{ scrolled: handleScroll }">
    <div class="nav_container">
      <a class="nav_logo" @click="scrollToPage('landing_page')"
        ><span class="logo_deco">J</span>INBOK LEE</a
      >
      <div class="nav_container_items">
        <div class="nav_container_menu">
          <a @click="scrollToPage('about_page')"
            ><span class="text_deco">01.</span>ABOUT</a
          >
          <a @click="scrollToPage('carousel_page')"
            ><span class="text_deco">02.</span>PORTFOLIO</a
          >
          <a @click="scrollToPage('contact_page')"
            ><span class="text_deco">03.</span>CONTACT</a
          >
          <button class="cover_letter_btn">COVER LETTER</button>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
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

    scrollToPage(id) {
      document.getElementById(id).scrollIntoView({
        behavior: "smooth",
      });
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
  height: 70px;
  padding: 1rem 0;
  z-index: 100;
  background: linear-gradient(to bottom, rgba(0, 0, 0, 0.7), transparent);
  transition: 0.5s;
  font-family: var(--font-mono);
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
  cursor: pointer;
  transition: 0.3s;
}

.nav_logo:hover {
  color: rgb(94, 239, 206);
  transition: 0.3s;
}

.logo_deco {
  color: rgb(94, 239, 206);
  text-shadow: rgb(255, 255, 255, 0.4) 3px 0px;
  font-size: 2.5rem;
  margin-right: 0.5rem;
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
  cursor: pointer;
  transition: 0.3s;
}

.nav_container_menu a:hover {
  color: rgb(94, 239, 206);
  transition: 0.3s;
}

.text_deco {
  color: rgb(94, 239, 206);
  margin-right: 0.7rem;
}

.cover_letter_btn {
  cursor: pointer;
  background: none;
  border: rgb(94, 239, 206) 1px solid;
  color: rgb(94, 239, 206);
  font-weight: bold;
  transition: 0.3s;
  padding: 0.8rem;
  font-family: var(--font-mono);
}

.cover_letter_btn:hover {
  background-color: rgb(94, 239, 206, 0.5);
  transition: 0.3s;
}
</style>
