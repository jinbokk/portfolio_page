<template>
  <div class="carousel-item" v-for="slide in slides"></div>
  <img :src="slide" />
</template>
