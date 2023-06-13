<template>
  <div class="container text-center col-12">
    <h1>Check what our client says about us</h1>
    <p class="text-black-50 text-center mt-5">
      Lorem ipsum dolor sit amet consectetur adipisicing elit. Nam, ullam! Lorem
      ipsum dolor sit amet consectetur adipisicing elit. Nam, ullam!
    </p>
  </div>
  <car-section></car-section>
  <div class="car2">
    <car-2-section></car-2-section>
  </div>
  <div class="footer">
    <footerFooter />
  </div>
</template>

<script>
import Car2Section from "../car2Section.vue";
import carSection from "./carSection.vue";
import footerFooter from "../footerFooter.vue";

export default {
  components: {
    carSection,
    Car2Section,
    footerFooter,
  },
};
</script>

<style scoped>
.car2 {
  margin-top: 200px;
}
.footer {
  margin-top: 0px;
}
</style>
