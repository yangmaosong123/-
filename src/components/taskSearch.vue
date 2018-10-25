<template>
     <div>
         <el-form :model="ruleForm" :rules="rules" ref="ruleForm" label-width="100px">
        <el-row>
          <el-col :span="6">
               <el-form-item label="公司名称">
          <el-select v-model="companyName" placeholder="请选择...">
            <el-option v-for="item in companyData" :key="item.id"></el-option>
          </el-select>
      </el-form-item>
          </el-col>
            <el-col :span="6">
                <el-form-item label="日期">
                    <el-date-picker  type="date" placeholder="选择日期" v-model="ruleForm.date"></el-date-picker>
                </el-form-item>
            </el-col>
            <el-col :span="3">
                <el-button type="primary">查询</el-button>
                <el-button type="warning">重置</el-button>
            </el-col>
        </el-row>
     
    </el-form>
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
             ruleForm:{
                data:"",
            },
        }
    }
}
</script>
