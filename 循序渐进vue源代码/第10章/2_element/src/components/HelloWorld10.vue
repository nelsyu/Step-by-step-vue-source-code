<template>
    <div class="hello">
        <el-alert title="成功提示的文案" type="success"> </el-alert>
        <br />
        <el-alert title="消息提示的文案" type="info"> </el-alert>
        <br />
        <el-alert title="警告提示的文案" type="warning"> </el-alert>
        <br />
        <el-alert title="错误提示的文案" type="error"> </el-alert>
    </div>
    <div class="hello">
        <el-button @click="popTip">弹出信息提示</el-button>
    </div>
    <div class="hello">
        <el-button @click="popAlert">弹出信息提示</el-button>
    </div>
    <div class="hello">
        <el-button @click="notify">弹出信息提示</el-button>

    </div>
    <div class="hello">

    </div>
</template>
  
<script>
export default {
    name: 'HelloWorld',
    data() {
        return {
 
        }
    },
    methods:{
        popTip() {
            this.$message({
                message: "提示内容",
                type: "warning",
            });
        },
        popAlert() {
            this.$msgbox({
                title: "提示",
                message: "详细的提示内容",
                type: "warning",
                showCancelButton: true,
                showConfirmButton: true,
                showInput: true,
            });
        },
        notify() {
            this.$notify({
                title: "通知标题",
                message: "通知内容",
                type: "success",
                duration: 3000,
                position: "top-right",
            });
        }
  }
}
</script>

<style>
    .hello {
        margin-top: 40px;
        text-align: left;
    }
</style>