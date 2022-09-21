<!-- eslint-disable vue/multi-word-component-names -->
<template>
  <section class="section_4">
    <div class="main_wrapper">
      <div class="sphere_wrapper"></div>
    </div>
  </section>
</template>

<script>
export default {
  mounted() {
    let x = 1;
    while (x <= 12) {
      let plane = document.createElement("div");
      plane.className = `plane plane-${x}`;
      plane.style.transform = `rotateY(${x * 15}deg)`;
      document.querySelector(".sphere_wrapper").appendChild(plane);
      for (let y = 1; y <= 36; y++) {
        let spoke = document.createElement("div");
        spoke.className = `spoke spoke-${y}`;
        spoke.innerHTML = `<div class="dot" style="background-color:${
          y % 2 === 0 ? "#00fffa" : "#ff9800"
        }; animation : pulsate .5s infinite ${aDelay(
          y
        )}s alternate both"></div>`;
        spoke.style.transform = `rotateZ(${y}0deg)`;
        document.querySelector(`.plane-${x}`).appendChild(spoke);
      }
      x++;
    }

    function aDelay(t) {
      switch (t) {
        case 1:
        case 35:
          return 0.05;

        case 2:
        case 34:
          return 0.1;

        case 3:
        case 33:
          return 0.15;

        case 4:
        case 32:
          return 0.2;

        case 5:
        case 31:
          return 0.25;

        case 6:
        case 30:
          return 0.3;

        case 7:
        case 29:
          return 0.35;

        case 8:
        case 28:
          return 0.4;

        case 9:
        case 27:
          return 0.45;

        case 10:
        case 26:
          return 0.5;

        case 11:
        case 25:
          return 0.55;

        case 12:
        case 24:
          return 0.6;

        case 13:
        case 23:
          return 0.65;

        case 14:
        case 22:
          return 0.7;

        case 15:
        case 21:
          return 0.75;

        case 16:
        case 20:
          return 0.8;

        case 17:
        case 19:
          return 0.85;

        case 18:
          return 0.95;

        case 36:
          return 0;

        default:
          return 1;
      }
    }
  },
};
</script>

<style>
.section_4 {
  position: absolute;
  top: 300vh;
  height: 100vh;
  width: 100vw;
  background-color: gray;
}

.main_wrapper {
  display: flex;
  position: absolute;
  transform-style: preserve-3d;
  perspective: 400px;
  inset: 0;
  align-items: center;
  justify-content: center;
}

.sphere_wrapper {
  transform-style: preserve-3d;
  width: 300px;
  height: 300px;
  position: relative;
  animation: rotate3d 15s linear infinite;
}

.plane {
  position: absolute;
  transform-style: preserve-3d;
  inset: 0;
}

.spoke {
  transform-origin: 0 0;
  transform-style: preserve-3d;
  position: absolute;
  left: 50%;
  top: 50%;
  height: 200px;
  width: 0;
}

.dot {
  position: absolute;
  width: 6px;
  height: 6px;
  border-radius: 50%;
  left: -3px;
  top: 100%;
  transform: rotateX(90deg);
}

@keyframes rotate3d {
  0% {
    transform: rotate3d(1, 1, 1, 0deg);
  }
  25% {
    transform: rotate3d(1, 1, 1, 90deg);
  }
  50% {
    transform: rotate3d(1, 1, 1, 180deg);
  }
  75% {
    transform: rotate3d(1, 1, 1, 270deg);
  }
  100% {
    transform: rotate3d(1, 1, 1, 360deg);
  }
}

@keyframes pulsate {
  0% {
    transform: rotateX(90deg) scale(0.3) translateZ(20px);
  }
  100% {
    transform: rotateX(90deg) scale(1) translateZ(0);
  }
}
</style>
