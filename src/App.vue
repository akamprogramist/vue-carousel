<template>
  <Carousel :slides="slides" :interval="3000" controls indicators></Carousel>
</template>

<script setup>
import Carousel from "./components/carousel/Carousel.vue";
const slides = [
  "https://picsum.photos/id/1032/900/400",
  "https://picsum.photos/id/1033/900/400",
  "https://picsum.photos/id/1037/900/400",
  "https://picsum.photos/id/1035/900/400",
  "https://picsum.photos/id/1036/900/400",
];
</script>
