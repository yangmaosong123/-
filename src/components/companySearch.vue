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
     <span style="font-weight:bold;">基础信息</span> 
    <el-table :data="tableData" border >
        <el-table-column label="板块/领域"></el-table-column>
        <el-table-column label="单位/项目名称"></el-table-column>
        <el-table-column label="自有员工总人数（人）"></el-table-column>
        <el-table-column label="安质环监督人员数量（人）"></el-table-column>
        <el-table-column label="承包商/供应商人数（人）"></el-table-column>
        <el-table-column label="当月员工工时数（万人工时）"></el-table-column>
        <el-table-column label="当月承包商工时数（万人工时）"></el-table-column>
    </el-table>
      <span style="font-weight:bold;">安质环绩效情况</span> 
    <el-table :data="tableData" border >
        <el-table-column label="板块/领域"></el-table-column>
        <el-table-column label="单位/项目名称"></el-table-column>
        <el-table-column label="死亡事故(人次)"></el-table-column>
        <el-table-column label="重伤事故（人次）"></el-table-column>
        <el-table-column label="轻伤事故（人次）"></el-table-column>
        <el-table-column label="限工事故(人次)"></el-table-column>
        <el-table-column label="医学处置事件(人次)"></el-table-column>
         <el-table-column label="急救箱事件(人次)"></el-table-column>
          <el-table-column label="重大未遂(起)"></el-table-column>
           <el-table-column label="一般未遂(起)"></el-table-column>
            <el-table-column label="其他财产损失事故（起）--无人员伤害但直接财产损失超100万"></el-table-column>
             <el-table-column label="因安质环事项被政府通报或处罚（次）"></el-table-column>
    </el-table>
    <span style="font-weight:bold;">安质环过程控制情况</span> 
    <el-table :data="tableData" border >
        <el-table-column label="板块/领域"></el-table-column>
        <el-table-column label="区域巡检覆盖率（%）"></el-table-column>
        <el-table-column label="安质环专题会议（次）"></el-table-column>
        <el-table-column label="安全培训（人次）"></el-table-column>
        <el-table-column label="安全投入（万元）"></el-table-column>
        <el-table-column label="应急演练（次）"></el-table-column>
        <el-table-column label="应急值班抽查在岗率（%)"></el-table-column>
         <el-table-column label="开展安质环经验反馈的次数（次）"></el-table-column>
          <el-table-column label="经验反馈纠正行动完成率（%）"></el-table-column>
    </el-table>
</div>
</template>

<script>
export default {
    data() {
        return {
            ruleForm:{
                data:"",
            },
            companyData:{},
            serach: function () {

            }
        }
    }
}
</script>
