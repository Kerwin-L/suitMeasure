<template >
    <div>
        <div class="container suit_style">
            <el-form :label-position="labelPosition" :rules="rules" ref="stitchwork" :label-width="labelWidth" :inline="false" :model="stitchwork" class="demo-form-inline">


                <el-form-item label="刺绣内容" prop="name">
                    <el-input v-model="stitchwork.name" placeholder="衬衫面料"></el-input>
                </el-form-item>

                <el-form-item label="纽扣颜色" prop="position">
                    <el-radio-group v-model="stitchwork.position">
                        <el-radio label="左袖口"></el-radio>
                        <el-radio label="右袖口"></el-radio>
                    </el-radio-group>
                </el-form-item>

                <el-form-item label="刺绣字体" prop="fontSize">
                    <el-select v-model="stitchwork.fontSize" placeholder="领型">
                        <el-option label="A1号" value="A1号"></el-option>
                        <el-option label="A2号" value="A2号"></el-option>
                        <el-option label="A3号" value="A3号"></el-option>
                        <el-option label="A4号" value="A4号"></el-option>
                        <el-option label="A5号" value="A5号"></el-option>
                    </el-select>
                </el-form-item>
                <el-form-item label="刺绣颜色" prop="fontColor">
                    <el-select v-model="stitchwork.fontColor" placeholder="领型">
                        <el-option label="紫色" value="紫色"></el-option>
                        <el-option label="棕色" value="棕色"></el-option>
                        <el-option label="蓝色" value="蓝色"></el-option>
                        <el-option label="绿色" value="绿色"></el-option>
                        <el-option label="红色" value="红色"></el-option>
                        <el-option label="粉红色" value="粉红色"></el-option>
                        <el-option label="白色" value="白色"></el-option>
                        <el-option label="黑色" value="黑色"></el-option>
                        <el-option label="灰色" value="灰色"></el-option>
                        <el-option label="深蓝色" value="红色"></el-option>
                        <el-option label="明绿色" value="白色"></el-option>
                    </el-select>
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

      //款式搭配
      suit_style:{
        suitSize: "", //衬衫规格
        processSeletion: "",//工艺选择
        suitType: "", //衬衫面料
        collarType: "",//领型
        cuffType: "",//袖型
        topFly: "",//门襟
        Hem: "",//下摆
        collectSuit: "",//收省
        collarColor: "",//领口颜色
        isPocket: false,//口袋选择
        fastenerType:"",//纽扣选择
        fastenerColor: "",//纽扣颜色
      },
      //量体数据
      measureInfo:{
        mNeck: null,//领围测量（命名下同）
        pNeck: null,//领围成衣（命名下同）
        mBust: null,//胸围
        pBust: null,//胸围
        mWaist: null,//腰围
        pWaist: null,//腰围
        mBelly: null,//肚围
        pBelly: null,
        mHipline: null,//臀围
        pHipline: null,
        mShoulderLength: null,//肩宽
        pShoulderLength: null,
        mCoatLength: null,//衣长
        pCoatLength: null,
        mSleeveLength: null,//长袖长
        pSleeveLength: null,
        mArm: null,//臂围
        pArm: null,
        mMiddleArm: null, //中臂围
        pMiddleArm: null,
        mWrist: null,//袖围
        pWrist: null,
      },
      specialSize:{
        bodyType: '', //体型
        frontOrBack: '', //前胸/后背
        shoulerSlopeQuantity: '', //肩斜量
        tummyType: '',//腹部量
        neckType: '',//脖子
        backType: '',//背部
      },
      stitchwork:{
        name:"",
        position: '',
        fontSize: "",
        fontColor: "",
      },
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
        name: [{ required: true, message: "请输入刺绣内容", trigger: "blur" }],

        position: [{ required: true, message: "请选择刺绣位置", trigger: "blur" }],
        fontSize: [{ required: true, message: "请选择刺绣字体", trigger: "blur" }],
        fontColor: [
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
