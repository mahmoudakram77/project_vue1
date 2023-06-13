<template>
  <div class="header"></div>

  <header>
    <nav>
      <div class="logo display-6">LOGO</div>
      <ul v-show="!mobile">
        <li v-for="menu in navbar" :key="menu.id" class="mt-1">
          <a class="link1" href="">{{ menu.name }}</a>
        </li>
        <div class="buttons" v-show="!mobile">
          <router-link to="/login">
            <button class="mx-2 btnn">Log In</button>
          </router-link>

          <button class="mx-2 btnn">Sign Up</button>
        </div>
      </ul>
      <div
        @click="toggleSpan"
        v-show="mobile"
        :class="{ 'icon-active': mobileNav }"
        class="burger"
      >
        <span></span>
        <span></span>
        <span></span>
      </div>
      <!-- mobile Nav -->
      <transition name="fade">
        <ul v-show="mobileNav" class="mobile-nav">
          <li v-for="menu in navbar" :key="menu.id">
            <a class="link2" href="">{{ menu.name }}</a>
          </li>
          <div class="buttons" v-show="!mobile">
            <button class="mx-2 btnn">Log In</button>
            <button class="mx-2 btnn">Sign Up</button>
          </div>
        </ul>
      </transition>
    </nav>
    <first-section />
  </header>
</template>

<script>
import firstSection from "./firstSection.vue";
export default {
  components: { firstSection },
  data() {
    return {
      navbar: [
        { id: 1, name: "Home", url: "#" },
        { id: 2, name: "About", url: "#" },
        { id: 3, name: "Page", url: "#" },
        { id: 4, name: "Services", url: "#" },
        { id: 5, name: "Case Study", url: "#" },
        { id: 6, name: "Contact", url: "#" },
      ],
      mobile: null,
      windowWidth: null,
      mobileNav: null,
    };
  },
  methods: {
    checkScreen() {
      this.windowWidth = innerWidth;
      if (this.windowWidth <= 990) {
        this.mobile = true;
        return;
      }
      this.mobile = false;
      this.mobileNav = false;
    },
    toggleSpan() {
      this.mobileNav = !this.mobileNav;
    },
  },
  created() {
    window.addEventListener("resize", this.checkScreen);
    this.checkScreen();
  },
};
</script>

<style lang="scss" scoped>
nav {
  margin: 20px 40px;
  display: flex;
  justify-content: space-between;

  ul {
    display: flex;
    list-style: none;

    li {
      margin: 0 10px;
      a {
        text-decoration: none;
        color: black;
      }
    }
  }
}

.buttons {
  a .btnn:first-child {
    background: rgb(71, 71, 255);
    padding: 3px 14px;
    border-radius: 20px;
    border: 1px solid rgb(71, 71, 255);
    color: white;
    transition: 0.5s ease all;

    &:hover {
      background: white;
      color: rgb(71, 71, 255);
      transition: 0.5s ease all;
      box-shadow: 0 0 20px rgb(71, 71, 255);
    }
  }
  .btnn:last-child {
    background: rgb(255, 255, 255);
    padding: 3px 10px;
    border-radius: 20px;
    border: 1px solid rgb(71, 71, 255);
    color: rgb(71, 71, 255);
    transition: 0.5s ease all;
    &:hover {
      background: rgb(71, 71, 255);
      color: white;
      transition: 0.5s ease all;
      box-shadow: 0 0 20px rgb(255, 255, 255);
    }
  }
}
.burger {
  display: inline-block;
  cursor: pointer;
  span {
    display: block;
    width: 25px;
    height: 3px;
    background: black;
    margin-bottom: 5px;
    border-radius: 20px;
    transition: transform 0.3s ease;
  }
}
.mobile-nav {
  /* background: blue; */
  position: absolute;
  left: 0;
  top: -20px;
  // height: 400px;
  padding: 30px;
  font-size: 20px;
  margin-top: 20px;
  width: 100%;
  z-index: 2;
  /* background: rgb(0, 95, 255); */
  background: white;
  opacity: 1;
}
.logo,
.icon-active {
  z-index: 3;
}

.mobile-nav {
  display: block;

  li {
    margin: 30px 0;
    text-align: center;
  }
}

// button for menu burger
.icon-active span:nth-child(1) {
  transform: translateY(8px) rotate(45deg) scale(1.1);
}

.icon-active span:nth-child(2) {
  opacity: 0;
}

.icon-active span:nth-child(3) {
  transform: translateY(-8px) rotate(-45deg) scale(1.1);
}
header {
  background: url(@/assets/header.png);
  width: 100%;
  height: 200%;
  background-size: cover;
  top: 0;
  position: absolute;
}
a {
}
.link1 {
  display: inline-block;
  z-index: 3;
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
.link1 {
  // display: inline-block;
  z-index: 3;
  color: rgb(255, 255, 255);

  &.link1:after {
    content: "";
    display: block;
    width: 0px;
    height: 1.2px;
    background: #fefefe;
    transition: 1s ease;
    border-radius: 20px;
  }
  &.link1:hover:after {
    width: 100%;
    transition: 1s ease;
  }
}
.link2 {
  display: inline-block;
  &.link2:after {
    content: "";
    display: block;
    width: 0px;
    height: 1.2px;
    background: black;
    transition: 1s ease all;
  }
  &.link2:hover:after {
    width: 100%;
  }
}
.link2 {
}
.fade-enter-from {
  opacity: 0;
}
.fade-enter-to {
  opacity: 1;
}
.fade-enter-active {
  transition: 1s ease all;
}
.fade-leave-active {
  transition: 0.3s ease all;
}
.fade-leave-from {
  opacity: 1;
  transform: translateX(0);
}
.fade-leave-to {
  opacity: 0;
  transform: translateX(-700px);
}
.mobile-nav a {
  animation: move 0.2s linear;
}

@keyframes move {
  from {
    transform: translateX(-700px);
  }
  to {
    transform: translateX(0);
  }
}
</style>
