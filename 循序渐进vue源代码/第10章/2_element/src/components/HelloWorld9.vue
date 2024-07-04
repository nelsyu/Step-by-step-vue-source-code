<template>
    <div class="hello">
        <el-time-picker
        size="large"
        :is-range="true"
        v-model="time"
        range-separator="~"
        :arrow-control="true"
        start-placeholder="开始时间"
        end-placeholder="结束时间"
        >
        </el-time-picker>
    </div>
    <div class="hello">
        <el-date-picker
        v-model="date"
        type="daterange"
        range-separator="至"
        start-placeholder="开始日期"
        end-placeholder="结束日期"
        >
        </el-date-picker>
    </div>
    <div class="hello">
        <el-color-picker :show-alpha="true" v-model="color"></el-color-picker>
    </div>
    <div class="hello">
    </div>
    <div class="hello">

    </div>
</template>
  
<script>
export default {
    name: 'HelloWorld',
    data() {
        return {
            time:"",
            date:"",
            color:""
        }
    },
    methods:{
        
  }
}
</script>

<style>
    .hello {
        margin-top: 40px;
        text-align: left;
    }
</style>