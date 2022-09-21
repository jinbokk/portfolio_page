<!-- eslint-disable vue/multi-word-component-names -->
<template>
  <section class="section_1">
    <h1 class="section_1_title">With<br />Infinite<br />Potential</h1>
    <div class="section_1_button">HELLO, JINBOK!</div>
  </section>
</template>

<script>
export default {};
</script>

<style>
.section_1 {
  position: fixed;
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

.section_1_title {
  font-size: 7rem;
  font-weight: bold;
  color: aliceblue;
}

.section_1_button {
  cursor: pointer;
  color: aliceblue;
  margin-top: 5rem;
  border: rgb(220, 220, 220) solid 1px;
  padding: 1rem;
  width: auto;
  box-shadow: inset 0 0 0 0 #98369a;
  transition: color 0.3s ease-in-out, box-shadow 0.3s ease-in-out;
}

.section_1_button:hover {
  box-shadow: inset 130px 0 0 0 #98369a;
  color: white;
}
</style>
