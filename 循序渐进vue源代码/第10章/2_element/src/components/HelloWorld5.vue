<template>
    <div class="hello">
        <el-radio v-model="radio" label="0">男</el-radio>
    <el-radio v-model="radio" label="1">女</el-radio>
    </div>
    <div class="hello">
        <el-radio-group v-model="radio2">
            <el-radio label="1">选项1</el-radio>
            <el-radio label="2">选项2</el-radio>
            <el-radio label="3">选项3</el-radio>
            <el-radio label="4">选项4</el-radio>
        </el-radio-group>
    </div>
    <div class="hello">
        <el-radio-group v-model="city">
            <el-radio-button label="1">北京</el-radio-button>
            <el-radio-button label="2">上海</el-radio-button>
            <el-radio-button label="3">广州</el-radio-button>
            <el-radio-button label="4">深圳</el-radio-button>
        </el-radio-group>
    </div>
    <div class="hello">
        <el-checkbox label="1" v-model="checkBox">A</el-checkbox>
        <el-checkbox label="2" v-model="checkBox">B</el-checkbox>
        <el-checkbox label="3" v-model="checkBox">C</el-checkbox>
        <el-checkbox label="4" v-model="checkBox">D</el-checkbox>
    </div>
    <div class="hello">
        <el-checkbox-group v-model="checkBox2" :min="1" :max="3">
            <el-checkbox label="1">A</el-checkbox>
            <el-checkbox label="2">B</el-checkbox>
            <el-checkbox label="3">C</el-checkbox>
            <el-checkbox label="4">D</el-checkbox>
        </el-checkbox-group>
    </div>
</template>
  
<script>
export default {
    name: 'HelloWorld',
    data() {
        return {
            radio:"0",
            radio2:"1",
            city:"1",
            checkBox:[],
            checkBox2:["1"],
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