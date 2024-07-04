<template>
    <div class="hello">
        <el-container>
        <el-header height="80px" style="background-color:gray">Header</el-header>
            <el-container>
                <el-aside width="200px" style="background-color:red">Aside</el-aside>
                <el-container>
                <el-main>
                    <div style="height:300px;background-color:#f1f1f1">内容</div>
                </el-main>
                <el-footer height="80px" style="background-color:gray">Footer</el-footer>
                </el-container>
            </el-container>
        </el-container>
    </div>
    <div class="hello">

    </div>
    <div class="hello">

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