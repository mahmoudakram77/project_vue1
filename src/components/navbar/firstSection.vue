<template>
  <div class="container">
    <div class="row">
      <div class="col-lg-6 col-sm-12 text-start">
        <h1 style="color: white">
          We Are On A Mission To Make Your
          <span style="color: orange">Business</span> Profitable
        </h1>
        <p class="text-black-50 mt-5">
          Lorem ipsum dolor sit amet consectetur adipisicing elit. Natus,
          praesentium!
        </p>
        <div class="parent">
          <div class="buttons">
            <button class="btn1 mt-3">Explore More</button>
            <button class="btn2 mx-2">Get Quote</button>
          </div>
        </div>
      </div>
      <div class="col-lg-6 col-sm-12 mt-5 move">
        <img class="img-fluid img-1" src="@/assets/header-one.png" alt="" />
      </div>
    </div>
  </div>

  <second-section />
</template>

<script>
import SecondSection from "./secondSection.vue";
export default {
  components: { SecondSection },
};
</script>

<style lang="scss" scoped>
.container {
  text-align: center;
  .row {
    align-items: center;
  }
}
@media screen and (max-width: 1200px) {
  h1 {
    text-align: center;
    margin-top: 100px;
  }
  p {
    text-align: center;
  }
  .parent {
    display: flex;
    justify-content: center;
  }
}
@media screen and (max-width: 1000px) {
  .img-1 {
    width: 460px;
  }
}

.btn1 {
  width: 120px;
  background: linear-gradient(rgb(255, 145, 0), rgb(238, 193, 109));
  border: transparent;
  padding: 5px;
  border: 1px solid orange;
  transition: 1s ease all;
  color: white;
  transition: 1s ease all;
  border-radius: 5px;
  &:hover {
    background: transparent;
    transition: 1s ease all;
  }
}
.btn2 {
  width: 120px;
  background: transparent;
  border: transparent;
  padding: 5px;
  border: 1px solid orange;
  color: white;
  transition: 1s ease all;
  border-radius: 5px;

  &:hover {
    background: linear-gradient(rgb(255, 145, 0), rgb(238, 193, 109));
    transition: 1s ease all;
  }
}

.move {
  animation: move 3s infinite alternate-reverse;
}
@keyframes move {
  0% {
    transform: translateY(20px);
  }
  100% {
    transform: translateY(-20px);
  }
}
</style>
