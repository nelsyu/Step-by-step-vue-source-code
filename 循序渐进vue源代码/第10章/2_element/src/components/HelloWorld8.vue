<template>
    <div class="hello">
        <div>
            <el-switch
            v-model="switch1"
            active-text="会员"
            inactive-text="非会员"
            active-color="#00FF00"
            inactive-color="#FF0000"
            ></el-switch>
        </div>
        <div>
            <el-switch
                v-model="switch2"
                active-text="加载中"
                :loading="true"
            ></el-switch>
        </div>
        <div>
            <el-switch
                v-model="switch3"
                inactive-text="禁用"
                :disabled="true"
            ></el-switch>
        </div>
    </div>
    <div class="hello">
        <el-slider v-model="sliderValue"></el-slider>
        <el-slider v-model="sliderValue" :format-tooltip="format"></el-slider>
    </div>
    <div class="hello">
        <el-slider
            v-model="sliderValue"
            :format-tooltip="format"
            :step="10"
            :show-stops="true"
            ></el-slider>
    </div>
    <div class="hello">
        <el-slider v-model="sliderValue" :marks="marks"></el-slider>
    </div>
    <div class="hello">

    </div>
</template>
  
<script>
export default {
    name: 'HelloWorld',
    data() {
        return {
            switch1:false,
            switch2:true,
            switch3:false,
            sliderValue:0,
            marks: {
                0: "起点",
                50: "半程啦！",
                90: {
                    style: {
                    color: "#ff0000",
                    },
                    label: "就到终点啦",
                }
            }
        }
    },
    methods:{
        format(value) {
            return `${value}%`;
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