<template lang="html">
  <div class="container form02">
      <el-form :label-position="labelPosition" :rules="rules" ref="form02" :label-width="labelWidth" :inline="false" :model="form2" class="demo-form-inline">
          <el-form-item label="文本框" prop="name">
              <el-input v-model="form2.name" placeholder="审批人"></el-input>
          </el-form-item>
          <el-form-item label="数字框" prop="amount">
              <el-input type="number" min="0" v-model="form2.amount" placeholder="金额"></el-input>
          </el-form-item>
          <el-form-item label="下拉框" prop="region">
              <el-select v-model="form2.region" placeholder="活动区域">
                  <el-option label="区域一" value="shanghai"></el-option>
                  <el-option label="区域二" value="beijing"></el-option>
              </el-select>
          </el-form-item>
          <el-form-item label="活动时间" prop="date1">
              <el-date-picker type="date" placeholder="选择日期" v-model="form2.date1" style="width: 100%;"></el-date-picker>
          </el-form-item>
          <el-form-item label="是否" prop="delivery">
              <el-switch v-model="form2.delivery"></el-switch>
          </el-form-item>

          <el-form-item label="多选按钮" prop="type">
              <el-checkbox-group v-model="form2.type">
                  <el-checkbox label="美食/餐厅线上活动" name="type"></el-checkbox>
                  <el-checkbox label="地推活动" name="type"></el-checkbox>
                  <el-checkbox label="线下主题活动" name="type"></el-checkbox>
                  <el-checkbox label="单纯品牌曝光" name="type"></el-checkbox>
              </el-checkbox-group>
          </el-form-item>
          <el-form-item label="单选按钮" prop="resource">
              <el-radio-group v-model="form2.resource">
                  <el-radio label="线上品牌商赞助"></el-radio>
                  <el-radio label="线下场地免费"></el-radio>
              </el-radio-group>
          </el-form-item>
          <el-form-item label="文本域" prop="desc">
              <el-input type="textarea" v-model="form2.desc"></el-input>
          </el-form-item>
          <el-form-item label=" ">
              <el-button type="primary" @click="onSubmit2">查询</el-button>
          </el-form-item>
      </el-form>
  </div>
</template>

<script>
export default {
}
</script>

<style lang="css">
</style>
