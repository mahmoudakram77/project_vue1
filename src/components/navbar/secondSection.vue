<template>
  <br />
  <br />
  <br />
  <br />
  <br />
  <br />
  <br />
  <div class="container text-center sec">
    <h1 class="text">We Are Specialized in the Following Services</h1>
    <p class="text-black-50">
      Lorem ipsum dolor sit amet consectetur adipisicing elit. Omnis, veritatis!
    </p>

    <div class="con d-flex mt-5">
      <div class="img1">
        <img src="@/assets/green1.png" alt="" />
      </div>
      <div class="img2">
        <img src="@/assets/green2.png" alt="" />
      </div>
      <div class="row mx-auto">
        <div class="col-lg-4 col-md-6">
          <div class="card">
            <div class="card-flex d-flex">
              <div class="card-icon"><i class="fa-brands fa-discord"></i></div>
              <div class="flex-c">
                <div class="card-title text-start mx-4">
                  Modern Keyword Analysis
                </div>
                <p class="text-black-50 text-start mx-4">
                  Lorem ipsum dolor sit amet consectetur adipisicing elit. Rem,
                  nobis.
                </p>
              </div>
            </div>
          </div>
        </div>
        <div class="col-lg-4 col-md-6">
          <div class="card">
            <div class="card-flex d-flex">
              <div class="card-icon"><i class="fa-brands fa-discord"></i></div>
              <div class="flex-c">
                <div class="card-title text-start mx-4">
                  Modern Keyword Analysis
                </div>
                <p class="text-black-50 text-start mx-4">
                  Lorem ipsum dolor sit amet consectetur adipisicing elit. Rem,
                  nobis.
                </p>
              </div>
            </div>
          </div>
        </div>
        <div class="col-lg-4 col-md-6">
          <div class="card">
            <div class="card-flex d-flex">
              <div class="card-icon"><i class="fa-brands fa-discord"></i></div>
              <div class="flex-c">
                <div class="card-title text-start mx-4">
                  Modern Keyword Analysis
                </div>
                <p class="text-black-50 text-start mx-4">
                  Lorem ipsum dolor sit amet consectetur adipisicing elit. Rem,
                  nobis.
                </p>
              </div>
            </div>
          </div>
        </div>
        <div class="col-lg-4 col-md-6">
          <div class="card">
            <div class="card-flex d-flex">
              <div class="card-icon"><i class="fa-brands fa-discord"></i></div>
              <div class="flex-c">
                <div class="card-title text-start mx-4">
                  Modern Keyword Analysis
                </div>
                <p class="text-black-50 text-start mx-4">
                  Lorem ipsum dolor sit amet consectetur adipisicing elit. Rem,
                  nobis.
                </p>
              </div>
            </div>
          </div>
        </div>
        <div class="col-lg-4 col-md-6">
          <div class="card">
            <div class="card-flex d-flex">
              <div class="card-icon"><i class="fa-brands fa-discord"></i></div>
              <div class="flex-c">
                <div class="card-title text-start mx-4">
                  Modern Keyword Analysis
                </div>
                <p class="text-black-50 text-start mx-4">
                  Lorem ipsum dolor sit amet consectetur adipisicing elit. Rem,
                  nobis.
                </p>
              </div>
            </div>
          </div>
        </div>
        <div class="col-lg-4 col-md-6">
          <div class="card">
            <div class="card-flex d-flex">
              <div class="card-icon"><i class="fa-brands fa-discord"></i></div>
              <div class="flex-c">
                <div class="card-title text-start mx-4">
                  Modern Keyword Analysis
                </div>
                <p class="text-black-50 text-start mx-4">
                  Lorem ipsum dolor sit amet consectetur adipisicing elit. Rem,
                  nobis.
                </p>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
  <div class="third">
    <thrirdSection />
  </div>
</template>

<script>
import thrirdSection from "./thrirdSection.vue";
export default {
  components: {
    thrirdSection,
  },
};
</script>

<style lang="scss" scoped>
.container {
  margin-top: 10px;
  /* max-width: 1000px; */
  position: absolute;
  top: 1200px;
  left: 50%;
  transform: translateX(-50%);
}
.text {
  color: rgb(0, 0, 81);
}
.con {
  background: rgb(252, 246, 246);
  padding: 20px;
  border-radius: 100px 0 100px 0;
  box-shadow: 0 0 20px rgb(194, 190, 190);
}

.card {
  width: 300px;
  height: 200px;
  margin: 10px auto;
  padding: 10px;
  border-radius: 50px 0 50px 0;
  border: 1px solid rgb(215, 214, 214);
  transition: 1s ease all;
  &:hover {
    box-shadow: 0 0 10px rgb(237, 203, 203);
    transform: scale(1.1);
    transition: 1s ease all;
  }
}
i {
  align-items: center;
  font-size: 30px;
  margin-top: 10px;
  background: rgba(255, 0, 0, 0.297);
  border-radius: 10px 0 10px 0;
}
.card-flex {
}
.img1 {
  position: absolute;
  z-index: -1;
  top: 80px;
  left: -50px;
}
.img2 {
  position: absolute;
  z-index: -1;
  bottom: -50px;
  right: -30px;
}
@media screen and (max-width: 992px) {
  .img1 {
    position: absolute;
    z-index: -1;
    top: 100px;
    left: -20px;
  }
}
@media screen and (max-width: 835px) {
  .img1 {
    position: absolute;
    z-index: -1;
    top: 70px;
    left: -30px;
  }
}
@media screen and (max-width: 768px) {
  .img1 {
    position: absolute;
    z-index: -1;
    top: 90px;
    left: -30px;
  }
}
@media screen and (max-width: 600px) {
  .img1 {
    position: absolute;
    z-index: -1;
    top: 140px;
    left: -10px;
  }
  .img2 {
    position: absolute;
    z-index: -1;
    bottom: -50px;
    right: 10px;
  }
  .con {
    max-width: 400px;
    margin: 0 auto;
  }
}
.third {
  margin-top: 1px;
}
@media screen and (max-width: 500px) {
  .sec {
    margin-top: 140px;
  }
}
</style>
