<template>
  <div class="side_bar_left_container">
    <a href="https://github.com/jinbokk" target="_blank">
      <img :src="github_icon" class="side_bar_icon" />
    </a>
    <a href="https://velog.io/@jinbokk" target="_blank">
      <img :src="velog_icon" class="side_bar_icon" />
    </a>
    <div class="deco_line">
      &#8213;&#8213;&#8213;&#8213;&#8213;&#8213;&#8213;&#8213;&#8213;&#8213;&#8213;
    </div>
  </div>
  <div class="side_bar_right_container">
    <a class="e_mail" href="mailto:eyelash1024@naver.com"
      >eyelash1024@naver.com</a
    >
    <div class="deco_line">
      &#8213;&#8213;&#8213;&#8213;&#8213;&#8213;&#8213;&#8213;&#8213;&#8213;&#8213;
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      github_icon: require("../assets/github_icon.png"),
      velog_icon: require("../assets/velog_icon.png"),
    };
  },
};
</script>
<style>
@keyframes sidebar_slideup {
  0% {
    opacity: 0;
    bottom: -100%;
  }

  50% {
    opacity: 0.5;
  }

  100% {
    opacity: 1;
    bottom: 0;
  }
}

.deco_line {
  margin-top: 2rem;
}

.side_bar_left_container {
  position: absolute;
  left: 3vw;
  bottom: 0;
  display: flex;
  align-items: center;
  justify-content: flex-end;
  writing-mode: vertical-rl;
  animation-duration: 1.4s;
  animation-name: sidebar_slideup;
}

.side_bar_right_container {
  position: absolute;
  right: 3vw;
  bottom: 0;
  display: flex;
  justify-content: flex-end;
  align-items: center;
  writing-mode: vertical-rl;
  font-family: var(--font-mono);
  animation-duration: 1.4s;
  animation-name: sidebar_slideup;
}

.e_mail {
  text-decoration: none;
  color: white;
  cursor: pointer;
  transition: 0.3s;
}

.e_mail:hover {
  color: rgb(94, 239, 206);
  transition: 0.3s;
  transform: translateY(-0.5rem);
}

.side_bar_icon {
  width: 25px;
  margin-top: 1.5rem;
  transition: 0.3s;
  cursor: pointer;
}

.side_bar_icon:hover {
  filter: invert(77%) sepia(33%) saturate(571%) hue-rotate(114deg)
    brightness(298%) contrast(101%);
  transition: 0.3s;
  transform: translateY(-0.5rem);
}
</style>
