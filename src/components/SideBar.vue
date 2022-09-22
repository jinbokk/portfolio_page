<template>
  <div class="side_bar_left_container">
    <img :src="github_icon" class="side_bar_icon" />
    <img :src="velog_icon" class="side_bar_icon" style="margin-right: 0" />
    <div class="deco_line">
      &#8213;&#8213;&#8213;&#8213;&#8213;&#8213;&#8213;&#8213;&#8213;&#8213;&#8213;
    </div>
  </div>
  <div class="side_bar_right_container">
    <div class="e_mail">eyelash1024@naver.com</div>
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
/* .side_bar_container_top {
  position: absolute;
  bottom: 0;
  width: 100vw;
  display: flex;
  justify-content: center;
  pointer-events: none;
}

.side_bar_container {
  width: 85vw;
  z-index: 10;
  display: flex;
  justify-content: space-between;
} */

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
}

.side_bar_right_container {
  position: absolute;
  right: 3vw;
  bottom: 0;
  display: flex;
  justify-content: flex-end;
  align-items: center;
  writing-mode: vertical-rl;
}

.e_mail {
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
