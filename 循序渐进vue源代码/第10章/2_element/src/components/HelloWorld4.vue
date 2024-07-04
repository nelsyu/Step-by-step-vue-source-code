<template>
    <div class="hello">
        <el-image style="width:500px" src="http://huishao.cc/img/head-img.png"></el-image>
    </div>
    <div class="hello">
        <el-image style="width:500px" src="http://huishao.cc/img/head-img.png">
            <template #placeholder>
                <h1>加载中...</h1>
            </template>
            <template #error>
                <h1>加载失败</h1>
            </template>
        </el-image>
    </div>
    <div class="hello">
        <!-- 使用文本类型的头像 -->
        <el-avatar style="margin:20px">用户</el-avatar>
        <!-- 使用图标类型的头像 -->
        <el-avatar style="margin:20px"><el-icon class="el-icon--soild"><User/></el-icon></el-avatar>
        <!-- 使用图片类型的头像 -->
        <el-avatar style="margin:20px" :size="100" src="http://huishao.cc/img/avatar.jpg"></el-avatar>
        <el-avatar style="margin:20px" src="http://huishao.cc/img/avatar.jpg"></el-avatar>
        <el-avatar style="margin:20px" shape="square"  src="http://huishao.cc/img/avatar.jpg"></el-avatar>
    </div>
</template>
  
<script>
export default {
    name: 'HelloWorld',
}
</script>

<style>
    .hello {
        margin-top: 40px;
        text-align: left;
    }
</style>