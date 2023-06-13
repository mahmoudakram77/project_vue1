<template>
  <div class="container1">
    <div class="third">
      <div class="container">
        <div class="row">
          <div class="col-lg-6 col-md-6 col-8">
            <img class="img-fluid" src="@/assets/1.png" alt="" />
          </div>
          <div class="col-lg-6 col-md-6 col-sm-12">
            <h1>Lorem ipsum dolor sit amet.</h1>
            <p>
              Lorem ipsum dolor sit, amet consectetur adipisicing elit.
              Repudiandae est blanditiis earum fugiat! Neque saepe, esse
              assumenda blanditiis aut incidunt.
            </p>
            <a class="link" href=""
              >Read More<i class="fa-solid fa-angle-right"></i
            ></a>
          </div>
        </div>
        <div class="row">
          <div class="col-lg-6 col-md-6 col-sm-12" id="text">
            <h1>Lorem ipsum dolor sit amet.</h1>
            <p>
              Lorem ipsum dolor sit, amet consectetur adipisicing elit.
              Repudiandae est blanditiis earum fugiat! Neque saepe, esse
              assumenda blanditiis aut incidunt.
            </p>
            <p>
              <i class="fa-solid fa-check mx-2"></i>Lorem ipsum dolor sit amet
              consectetur adipisicing elit.
            </p>
            <p>
              <i class="fa-solid fa-check mx-2"></i>Lorem ipsum dolor sit amet
              consectetur adipisicing elit.
            </p>

            <p>
              <i class="fa-solid fa-check mx-2"></i>Lorem ipsum dolor sit amet
              consectetur adipisicing elit
            </p>

            <a class="mx-4 link" href=""
              >Read More<i class="fa-solid fa-angle-right mx"></i
            ></a>
          </div>
          <div class="col-lg-6 col-md-6 col-8" id="img">
            <img class="img-fluid" src="@/assets/2.png" alt="" />
          </div>
        </div>
      </div>
    </div>
  </div>

  <div class="container con3">
    <div class="row con3">
      <div class="col-lg-6">
        <img class="img-fluid move mx-5" src="@/assets/3.png" alt="" />
      </div>
      <div class="col-lg-6">
        <h1 style="color: black">Lorem ipsum dolor sit amet.</h1>
        <p style="color: black">
          Lorem ipsum dolor sit amet, consectetur adipisicing elit. Laborum,
          aperiam. Lorem ipsum dolor sit amet, consectetur adipisicing elit.
          Laborum, aperiam.
        </p>
        <p style="color: black">
          <i style="color: orange" class="fa-solid fa-check mx-2"></i>Lorem
          ipsum dolor sit amet consectetur.
        </p>
        <p style="color: black">
          <i style="color: orange" class="fa-solid fa-check mx-2"></i>Lorem
          ipsum dolor sit amet consectetur.
        </p>
        <p style="color: black">
          <i style="color: orange" class="fa-solid fa-check mx-2"></i>Lorem
          ipsum dolor sit amet consectetur.
        </p>
        <a class="mx-3 link" style="color: blue" href="">Read More</a>
      </div>
    </div>
  </div>
  <div class="four">
    <four-section></four-section>
  </div>
</template>

<script>
import fourSection from "./fourSection.vue";
export default {
  components: { fourSection },
};
</script>

<style lang="scss" scoped>
.col-lg-6 img {
}
.third {
  background-image: url(@/assets/bg-orange.png);
  height: 2200px;
}
.container {
  position: relative;
  top: 400px;
}
.row {
  justify-content: center;
  align-items: center;
}

i,
h1,
p,
a {
  color: white;
  text-decoration: none;
}

.link {
  display: inline-block;

  color: rgb(255, 255, 255);

  &:after {
    content: "";
    display: block;
    width: 0px;
    height: 1.2px;
    background: #ffffff;
    transition: 1s ease;
    border-radius: 20px;
  }
  &:hover:after {
    width: 100%;
    transition: 1s ease;
  }
}
.col-lg-6 {
  margin-top: 100px;
}
@media screen and (max-width: 768px) {
  .third {
    margin-top: 1000px;
  }
  #text {
    order: 2;
  }
}
.container1 {
  position: relative;
  top: 1000px;
}
.con3 {
  margin-top: 300px;
}
.con3 {
  align-items: center;
  justify-content: center;
  text-align: center;
}
.four {
  margin-top: 500px;
}
@media screen and (max-width: 500px) {
  .col-lg-6 {
    margin-top: 50px;
  }
}
.con3 {
  overflow: hidden;
}
</style>
