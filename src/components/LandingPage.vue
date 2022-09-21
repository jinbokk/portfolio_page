<!-- eslint-disable vue/multi-word-component-names -->
<template>
  <div class="landing_page">
    <h1 class="landing_page_title">With<br />Infinite<br />Potential</h1>
    <div class="landing_page_button">HELLO, JINBOK!</div>
  </div>
</template>

<script>
export default {};
</script>

<style>
.landing_page {
  position: fixed;
  top: 0;
  height: 100vh;
  width: 100vw;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  text-align: center;
  line-height: 1.5;
  font-weight: bold;
  background-color: rgb(105, 25, 255);
}

.landing_page_title {
  font-size: 7rem;
  font-weight: bold;
  color: aliceblue;
}

.landing_page_button {
  cursor: pointer;
  color: aliceblue;
  margin-top: 5rem;
  border: rgb(220, 220, 220) solid 1px;
  padding: 1rem;
  width: auto;
  box-shadow: inset 0 0 0 0 #98369a;
  transition: color 0.3s ease-in-out, box-shadow 0.3s ease-in-out;
}

.landing_page_button:hover {
  box-shadow: inset 130px 0 0 0 #98369a;
  color: white;
}
</style>
