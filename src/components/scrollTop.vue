<template>
  <transition name="fade">
    <div class="btn" @click="scrollToTop" v-show="show">
      <i class="fa-solid fa-circle-chevron-up"></i>
    </div>
  </transition>
</template>

<script>
export default {
  data() {
    return {
      show: false,
    };
  },

  methods: {
    scrollToTop() {
      window.scrollTo({ top: 0, behavior: "smooth" });
    },
    onScroll() {
      this.show = window.scrollY >= 500;
    },
  },

  created() {
    window.addEventListener("scroll", this.onScroll);
    this.onScroll();
  },

  beforeDestroy() {
    window.removeEventListener("scroll", this.onScroll);
  },
};
</script>

<style scoped>
.btn {
  position: fixed;
  right: 10px;
  bottom: 0px;
  font-size: 40px;
}
.fade-enter-from {
  transform: translateY(100px);
}
.fade-enter-to {
  transform: translateY(0px);
}
.fade-enter-active {
  transition: 1s ease all;
}
.fade-leave-from {
  transform: translateY(0px);
}
.fade-leave-to {
  transform: translateY(100px);
}
.fade-leave-active {
  transition: 0.5s ease all;
}
i {
  color: orange;
}
</style>
