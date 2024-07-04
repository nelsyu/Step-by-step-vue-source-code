<template>
    <div class="hello">
        <el-input v-model="value" 
            placeholder="请输入内容"
            :disabled="false"
            :show-password="true"
            :clearable="true"
            prefix-icon="Search"
            type="text"></el-input>
    </div>
    <div class="hello">
        <el-input v-model="value2" type="text">
            <template #prepend>Http://</template>
            <template #append>.com</template>
        </el-input>
    </div>
    <div class="hello">
        <el-autocomplete v-model="value3" 
            :fetch-suggestions="queryData"
            placeholder="请输入内容"
            @select="selected"
            :highlight-first-item="true"
        ></el-autocomplete>
    </div>
    <div class="hello">
        <el-input-number :min="1" :max="10" :step="1" v-model="num"></el-input-number>
    </div>
    <div class="hello">

    </div>
</template>
  
<script>
export default {
    name: 'HelloWorld',
    data() {
        return {
            value:"",
            value2:"",
            value3:"",
            num:1
        }
    },
    methods:{
        queryData(queryString, callback) {
            let array = []
            if (queryString.length > 0) {
                array.push({value:queryString}) 
            }
            array.push(...[{value:"衣服"},{value:"裤子"},{value:"帽子"},{value:"鞋子"}])
            callback(array) 
        },
        selected(obj) {
            alert(obj.value)
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