<template>
  <div class="carousel">
    <div class="carousel-inner">
      <CarouselItem
        v-for="(slide, index) in slides"
        :key="`item-${index}`"
        :slide="slide"
        :current-slide="currentSlide"
        :index="index"
      ></CarouselItem>
    </div>
  </div>
</template>
<script setup>
import { ref } from "vue";
import { onMounted } from "vue";
import CarouselItem from "./CarouselItem.vue";
const props = defineProps(["slides"]);
const currentSlide = ref(0);
const slideInterval = ref(null);
onMounted(()=>{
    this.slideInterval = setInterval(()=>{
        const index = this.currentSlide < this.slides.length -1 ? this.currentSlide +1 :0;
        this.currentSlide=index;
    },3000)

}),
beforeUnmount(()=> {
    clearInterval(this.slideInterval);
}),
</script>

<style scoped>
.carousel {
  display: flex;
  justify-content: center;
}
.carousel-inner {
  position: relative;
  width: 900px;
  height: 400px;
  overflow: hidden;
}
</style>
