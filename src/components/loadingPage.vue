<template>
  <div class="loading" v-if="showing">
    <img src="@/assets/giphy.gif" alt="" />
  </div>
</template>

<script>
export default {
  data() {
    return {
      showing: false,
    };
  },
  methods: {
    show() {
      this.showing = true;

      setTimeout(() => {
        this.showing = false;
      }, 3000);
    },
  },
  mounted() {
    this.show();
  },
};
</script>

<style>
.loading {
  background: white;
  display: flex;
  position: absolute;
  left: 50%;
  top: 50%;
  align-items: center;
  justify-content: center;
  transform: translate(-50%, -50%);
  width: 100%;
  height: 500%;
  z-index: 9999;
}
</style>
