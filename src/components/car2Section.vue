<template>
  <Carousel v-bind="settings" :breakpoints="breakpoints">
    <Slide v-for="slide in images" :key="slide.id">
      <div class="carousel__item">
        <img :src="slide.url" alt="" />
      </div>
    </Slide>

    <template #addons>
      <Navigation />
    </template>
  </Carousel>
</template>

<script>
import { defineComponent } from "vue";
import { Carousel, Slide } from "vue3-carousel";

import "vue3-carousel/dist/carousel.css";

export default defineComponent({
  name: "Breakpoints",
  components: {
    Carousel,
    Slide,
  },
  data: () => ({
    images: [
      { id: 1, url: require("@/assets/11.png") },
      { id: 2, url: require("@/assets/12.png") },
      { id: 3, url: require("@/assets/13.png") },
      { id: 4, url: require("@/assets/14.png") },
      { id: 5, url: require("@/assets/16.png") },
    ],
    // carousel settings
    settings: {
      itemsToShow: 2,
      snapAlign: "center",
      autoplay: 2000,
      wrapAround: true,
      transition: 3000,
    },
    // breakpoints are mobile first
    // any settings not specified will fallback to the carousel settings
    breakpoints: {
      // 700px and up
      700: {
        itemsToShow: 3.5,
        snapAlign: "center",
      },
      // 1024 and up
      1024: {
        itemsToShow: 4,
        snapAlign: "start",
      },
    },
  }),
});
</script>
