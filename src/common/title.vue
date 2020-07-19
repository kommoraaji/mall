<template>
  <div>
    <div class="nav-bar">
      <button class="btn" @click="goBack">
        <van-icon name="arrow-left" />
      </button>
      <span class="nav-span">{{this.$route.name}}</span>
      <button class="btn1">
        <van-icon name="ellipsis" />
      </button>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {};
  },
  methods: {
    goBack() {
      this.$router.go("-1");
    }
  },
  mounted() {},
  watch: {}
};
</script>

<style lang="" scoped>
.nav-bar {
  position: relative;
  width: 100%;
  height: 0.9rem;
  line-height: 0.9rem;
  text-align: center;
  background: #f26b11;
}
.nav-bar .btn {
  position: absolute;
  top: 0;
  left: 0;
  width: 0.7rem;
  height: 0.7rem;
  background: transparent;
  border: none;
}
.nav-bar .btn1 {
  position: absolute;
  top: 0;
  right: 0;
  width: 0.7rem;
  height: 0.7rem;
  background: transparent;
  border: none;
}
.nav-bar .nav-span {
  color: #fff;
  font-size: 0.32rem;
}
.btn,
.btn1 {
  margin: 0.08rem;
  font-size: 0.36rem;
  color: #fff;
}
.btn1 {
  font-size: 0.52rem;
}
</style>