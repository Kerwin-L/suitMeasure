<template >
    <div>
        <div class="container suit_style">
            <el-form :label-position="labelPosition" :rules="rules" ref="customerInfo" :label-width="labelWidth" :inline="false" :model="customerInfo" class="demo-form-inline">


                <el-form-item label="年龄" prop="age">
                    <el-input v-model="customerInfo.age" placeholder="请输入年龄"></el-input>
                </el-form-item>
                <el-form-item label="身高" prop="height">
                    <el-input v-model="customerInfo.height" placeholder="请输入身高"></el-input>
                </el-form-item>
                <el-form-item label="体重" prop="weight">
                    <el-input v-model="customerInfo.weight" placeholder="请输入体重"></el-input>
                </el-form-item>
                <el-form-item label="邮寄地址" prop="address">
                    <el-input v-model="customerInfo.address" placeholder="请输入邮寄地址"></el-input>
                </el-form-item>



                <el-form-item label=" ">
                    <el-button type="primary" @click="onSubmit2">查询</el-button>
                </el-form-item>
            </el-form>
        </div>
        <!-- 查询区----end -->
    </div>
</template>
<style lang="scss">
// 设置输入框的宽度
.form01 {
  .el-form-item__content {
    width: 220px;
    .el-select {
      width: 220px;
    }
  }
}
.suit_style {
  .el-form-item__content {
    width: 430px;
    .el-select {
      width: 430px;
    }
  }
}
.form03 {
  .el-form-item__content {
    width: 220px;
    .el-select {
      width: 220px;
    }
  }
}
.el-checkbox-group .el-checkbox {
  margin-left: 0;
  padding-right: 30px;
}
</style>
<script>
export default {
  name: "searchinput",
  data() {
    return {
      customerInfo:{
        age: null,
        height: null,
        weight: null,
        address: null,
      },
      labelPosition: "right", //lable对齐方式
      labelWidth: "80px", //lable宽度
      rules: {
        // name: [
        //   { required: true, message: "请输入活动名称", trigger: "blur" },
        //   { min: 3, max: 5, message: "长度在 3 到 5 个字符", trigger: "blur" }
        // ],
        age: [{ required: true, message: "请输入刺绣内容", trigger: "blur" }],

        height: [{ required: true, message: "请选择刺绣位置", trigger: "blur" }],
        weight: [{ required: true, message: "请选择刺绣字体", trigger: "blur" }],
        address: [
          { required: true, message: "请选择刺绣颜色", trigger: "change" }
        ],

      }
    };
  },
  methods: {
    onSubmit1() {
      this.$message({
        type: "success",
        message: "表单提交成功"
      });
    },
    //表单2提交
    onSubmit2() {
      this.$refs["suit_style"].validate(valid => {
        if (valid) {
          this.$alert("表单验证通过，提交成功", "标题名称", {
            confirmButtonText: "确定",
            callback: action => {
              //   this.$message({
              //     type: "info",
              //     message: `action: ${action}`
              //   });
            }
          });
        } else {
          console.log("error submit!!");
          return false;
        }
      });
    },
    onSubmit3() {
      this.$message({
        type: "success",
        message: "表单提交成功"
      });
    }
  }
};
</script>
