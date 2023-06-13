<template>
  <div class="footer">
    <div class="background">
      <div class="container position-relative">
        <div class="row">
          <div class="mmm">
            <div class="col-lg-12 mm">
              <h1 style="color: white">NewLetter</h1>
              <p style="color: white">
                Lorem ipsum dolor sit amet, consectetur adipisicing elit.
                Cupiditate, impedit!
              </p>
              <input type="text" />
              <button>Submit</button>
              <div class="iconn mt-3" style="font-size: 50px; color: white">
                <a href=""> <i class="fa-brands fa-facebook mx-3"></i></a>
                <a href=""> <i class="fa-brands fa-twitter mx-3"></i></a>
                <a href=""> <i class="fa-brands fa-linkedin mx-3"></i></a>
              </div>
            </div>
          </div>
          <div class="middle"></div>
          <div class="row text-center mt-5">
            <div class="col-lg-3 col-md-3">
              <div class="title text-center">
                <h1>company</h1>
                <p>About</p>
                <p>Program</p>
                <p>Jobs</p>
                <p>Blogs</p>
              </div>
            </div>
            <div class="col-lg-3 col-md-3">
              <h1>Resourse</h1>
              <p>Support</p>
              <p>Development</p>
              <p>Contact</p>
              <p>Term</p>
              <p>Live Chat</p>
            </div>
            <div class="col-lg-3 col-md-3">
              <h1>Contact</h1>
              <p>Lorem ipsum dolor sit amet.</p>
              <p>mahmoudeljaru@gmail.com</p>
              <p>+970500085385</p>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style lang="scss" scoped>
.mmm {
  // margin: 0 auto;
  text-align: center;
}
.footer {
  /* Add some padding to the footer for visibility */

  .container {
    .row {
      justify-content: center;
    }
  }
}
ul {
  list-style: none;
}
input {
  padding: 5px;
  border-radius: 10px 0px 0px 10px;
  border: none;
  box-shadow: 0 0 3px rgb(255, 255, 255);
}
button {
  background: blue($color: #000000);
  border: none;
  box-shadow: 0 0 3px rgb(255, 255, 255);
  border-radius: 0px 10px 10px 0px;
  padding: 5px;
}

@media screen and (max-width: 500px) {
  .footer {
    display: flex;
  }
  .row {
    margin: 0 auto;
    justify-content: center;
    text-align: center;
  }
}
.two {
  margin: 0 auto;
  justify-content: center;
  text-align: center;
}
.background {
  background-image: url("@/assets/Bg.png");
  background-repeat: no-repeat;
  background-size: cover;
  background-position: center;
  // height: 1000px;

  /* Add the desired background properties here */
}
.row {
}
.mmm {
  margin-top: 500px;
}
a {
  color: white;
}
button {
  color: white;
}
h1,
h2,
h3,
h4,
p {
  color: white;
}
</style>
