<template>
  <h1>HelloWorld</h1>
  <p>
    <!-- route-link是路由跳转组件，用to来指定要跳转的路由 -->
    <router-link to="/demo1">页面一</router-link>
    <br/>
    <router-link to="/demo2">页面二</router-link>
  </p>
  <p>
    <router-link to="/user/小王/8888">小王</router-link>
    <br/>
    <router-link to="/user/小李/6666">小李</router-link>
  </p>
    <p>
      <el-button type="primary" @click="toUser">中户中心</el-button>
    </p>
  <!-- router-view是路由的页面出口，路由匹配到的组件会渲染在此  -->
  <router-view></router-view>
  <el-container>
    <el-header height="80px">
      <router-view name="topBar"></router-view>
    </el-header>
    <el-main>
      <router-view name="main"></router-view>
    </el-main>
  </el-container>
</template>
<script>
export default {
  name: 'App',
  components: {
    
  },
  methods:{
    toUser() {
      this.$router.push({
        path:"/user/小王"
      })
    }
  }
}
</script>