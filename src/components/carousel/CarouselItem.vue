<template>
  <div class="carousel-item" v-show="currentSlide === index">
    <img :src="slide" alt="" />
  </div>
</template>

<script setup>
const props = defineProps(["slide", "currentSlide", "index"]);
</script>

<style>
.carousel-item {
  position: relative;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
}
</style>
