<template>
  <div class="ddd" v-if="true">
    <Carousel v-bind="settings">
      <Slide v-for="item in images" :key="item.id">
        <div class="carousel__item">
          <!-- <img :src="item.url" alt="Carousel Item" /> -->
          <div class="card mt-5">
            <div class="card-body text-start mx-3">
              <div class="card-img">
                <img :src="item.url" alt="" />
                <div class="card-text">
                  <h3>{{ item.name }}</h3>
                  <h5>{{ item.job }}</h5>
                  <p class="text-black-50">{{ item.desc }}</p>
                </div>
              </div>
            </div>
          </div>
        </div>
      </Slide>

      <template #addons>
        <Navigation class="custom-navigation" />
        <Pagination class="custom-pagination mt-4" />
      </template>
    </Carousel>
  </div>

  <!-- :autoplay="2000"
      :itemsToShow="2.5"
      :wrapAround="true" -->
</template>

<script>
import { defineComponent } from "vue";
import { Carousel, Navigation, Slide, Pagination } from "vue3-carousel";

import "vue3-carousel/dist/carousel.css";

export default defineComponent({
  name: "WrapAround",
  components: {
    Carousel,
    Slide,
    Navigation,
    Pagination,
  },
  data() {
    return {
      images: [
        {
          id: 1,
          url: require("@/assets/4.png"),
          name: "mahmoud",
          job: "Ceo",
          desc: "Lorem ipsum, dolor sit amet consectetur adipisicing elit. Odio, quis.",
        },
        {
          id: 2,
          url: require("@/assets/5.png"),
          name: "mahmoud1",
          job: "web developer",
          desc: "Lorem ipsum, dolor sit amet consectetur adipisicing elit. Odio, quis.",
        },
        {
          id: 2,
          url: require("@/assets/6.png"),
          name: "soso",
          job: "web design",
          desc: "Lorem ipsum, dolor sit amet consectetur adipisicing elit. Odio, quis.",
        },
        {
          id: 2,
          url: require("@/assets/5.png"),
          name: "mahmoud3",
          job: "engineer",
          desc: "Lorem ipsum, dolor sit amet consectetur adipisicing elit. Odio, quis.",
        },
        {
          id: 2,
          url: require("@/assets/4.png"),
          name: "mahmoud4",
          job: "programming",
          desc: "Lorem ipsum, dolor sit amet consectetur adipisicing elit. Odio, quis.",
        },
      ],
      settings: {
        itemToShow: 1,
        snapAlign: "center",
        autoplay: 2000,
        wrapAround: true,
        transition: 1000,
        breakpoints: {
          700: {
            itemsToShow: 2.5,
            snapAlign: "center",
          },
          1024: {
            itemsToShow: 3,
            snapAlign: "center",
          },
        },
      },
    };
  },
});
</script>

<style lang="scss">
.custom-navigation {
  color: rgb(255, 255, 255);
  font-size: 18px;
  background: rgb(0, 0, 0);
  border-radius: 20px;
  &:hover {
    color: white;
  }
}

.ddd {
  margin: 0 auto;
}
.card {
  width: 300px;
  border-radius: 100px 0 100px 0;
  border: none;
  box-shadow: 0 0 5px rgb(150, 150, 150);
  margin-bottom: 10px;
}
</style>
