<template>
<el-container>
    <el-aside width="200px">
        <el-menu default-active="1" class="el-menu-vertical-demo"   text-color="#fff" active-text-color="#ffd04b">
            <el-menu-item index="1">
                <router-link to="/companyReport">公司指标报表</router-link>
            </el-menu-item>
            <el-menu-item index="2" >
                 <router-link to="/taskTracking">重点任务跟踪</router-link>
            </el-menu-item>
             <el-menu-item index="3" >
                 <router-link to="/companySearch">公司指标报表查询</router-link>
            </el-menu-item>
             <el-menu-item index="4" >
                 <router-link to="/taskSearch">重点任务跟踪查询</router-link>
            </el-menu-item>
        </el-menu>
    </el-aside>
    <el-main>
        <router-view></router-view>
    </el-main>
</el-container>
</template>

<script>
export default {
    data() {
        return {

        }
    }
}
</script>
