<template>
  <nav-bar></nav-bar>
  <scroll-top></scroll-top>
  <loading-page />
</template>

<script>
import navBar from "@/components/navbar/navBar.vue";
import ScrollTop from "@/components/scrollTop.vue";
import loadingPage from "@/components/loadingPage.vue";

export default {
  components: {
    navBar,
    ScrollTop,
    loadingPage,
  },
};
</script>
, LoadingPage
