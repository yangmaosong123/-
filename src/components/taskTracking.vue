<template>
    <div>
        <span style="font-weight:bold;">重点工作开展情况</span>
       <el-table :data="tableData" border>
         <el-table-column label="序号" prop="id"></el-table-column>
         <el-table-column label="工作任务名称" prop="workName"></el-table-column>
         <el-table-column label="具体内容" prop="content"></el-table-column>
         <el-table-column label="承接板块/单位" prop="company"></el-table-column>
         <el-table-column label="承接部门/负责人" prop="people"></el-table-column>
         <el-table-column label="任务最新进展" prop="task"></el-table-column>
         <el-table-column label="完成率" prop="completion"></el-table-column>
         <el-table-column label="操作">
             <template slot-scope="scope">
                 <el-button type="warning" @click="handleEdit(scope.row)">编辑</el-button>
             </template>
         </el-table-column>
       </el-table>

         <span style="font-weight:bold;">良好实践推荐清单</span>
        <el-table :data="tableData2" border>
         <el-table-column label="序号" prop="id"></el-table-column>
         <el-table-column label="良好实践名称" prop="name"></el-table-column>
         <el-table-column label="良好实践的具体内容" prop="content"></el-table-column>
         <el-table-column label="推荐板块/内容" prop="plate"></el-table-column>
         <el-table-column label="推荐部门/负责人" prop="people"></el-table-column>
         <el-table-column label="主要亮点" prop="primary"></el-table-column>
         <el-table-column label="优先度" prop="priority"></el-table-column>
         <el-table-column label="操作">
             <template slot-scope="scope">
                 <el-button type="warning" @click="handleEdit2(scope.row)">编辑</el-button>
             </template>
         </el-table-column>
       </el-table>
    </div>
    
</template>
<script>
export default {
    data(){
        return{
            tableData:[
                {
                 id:"1",
                 workName:"安质环安装",
                 content:"安质环安装",
                 company:"大亚湾公司",
                 people:"张三",
                 task:"进入收尾阶段",
                 completion:"95%",
                }
            ],
           tableData2:[{
               id:"1",
               name:"安质环拆除",
               content:"安质环拆除",
               plate:"核电板块",
               people:"李四",
               primary:"快速，安全，有效",
               priority:"最优先级别",
           }] 
        }
    }
}
</script>
