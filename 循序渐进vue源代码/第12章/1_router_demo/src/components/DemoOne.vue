<template>
    <h1>示例页面1</h1>
    <el-button type="primary" @click="click">跳转Demo2</el-button>
</template>
<script>
import Demo2 from "./DemoTwo.vue";
export default {
  created() {
    console.log(this);
    this.$router.addRoute({
      path: "/demo2",
      component: Demo2,
    });
  },
  methods: {
    click() {
      this.$router.push("/demo2");
    },
  },
  beforeRouteEnter(to, from) {
    console.log(to, from, "前置守卫");
    return true;
  },
  beforeRouteUpdate(to, from) {
    console.log(to, from, "路由参数有更新时的守卫");
  },
  beforeRouteLeave(to, from) {
    console.log(to, from, "离开页面");
  },
};
</script>