<template >
    <div>
      纵向双列表单:
            <!-- 查询区----start -->
            <div class="container" style="width: 660px;">
                <el-form :label-position="labelPosition" :rules="rules" :label-width="labelWidth" :inline="true" :model="measureInfo" class="demo-form-inline">
                  <el-form-item label="领围测量" prop="mNeck">
                      <el-input type="number" min="30"  v-model="measureInfo.mNeck" placeholder="范围30-60"></el-input>
                  </el-form-item>
                 <el-form-item label="领围成衣" prop="pNeck">
                      <el-input type="number" min="30"  v-model="measureInfo.pNeck" placeholder=""></el-input>
                  </el-form-item>

                  <el-form-item label="胸围测量" prop="mBust">
                      <el-input type="number" min="30"  v-model="measureInfo.mBust" placeholder=""></el-input>
                  </el-form-item>
                 <el-form-item label="胸围成衣" prop="pBust">
                      <el-input type="number" min="0" v-model="measureInfo.pBust" placeholder=""></el-input>
                  </el-form-item>

                  <el-form-item label="腰围测量" prop="mWaist">
                      <el-input type="number" min="30" v-model="measureInfo.mWaist" placeholder=""></el-input>
                  </el-form-item>
                 <el-form-item label="腰围成衣" prop="pWaist">
                      <el-input type="number" min="0" v-model="measureInfo.pWaist" placeholder=""></el-input>
                  </el-form-item>

                  <el-form-item label="肚围测量" prop="mBelly">
                      <el-input type="number" min="30" v-model="measureInfo.mBelly" placeholder=""></el-input>
                  </el-form-item>
                 <el-form-item label="肚围成衣" prop="pBelly">
                      <el-input type="number" min="0" v-model="measureInfo.pBelly" placeholder=""></el-input>
                  </el-form-item>

                  <el-form-item label="臀围测量" prop="mHipline">
                      <el-input type="number" min="30" v-model="measureInfo.mHipline" placeholder=""></el-input>
                  </el-form-item>
                 <el-form-item label="臀围成衣" prop="pHipline">
                      <el-input type="number" min="0" v-model="measureInfo.pHipline" placeholder=""></el-input>
                  </el-form-item>

                  <el-form-item label="肩宽测量" prop="mShoulderLength">
                      <el-input type="number" min="30" v-model="measureInfo.mShoulderLength" placeholder=""></el-input>
                  </el-form-item>
                 <el-form-item label="肩宽成衣" prop="pShoulderLength">
                      <el-input type="number" min="0" v-model="measureInfo.pShoulderLength" placeholder=""></el-input>
                  </el-form-item>

                  <el-form-item label="衣长测量" prop="mCoatLength">
                      <el-input type="number" min="30" v-model="measureInfo.mCoatLength" placeholder=""></el-input>
                  </el-form-item>
                 <el-form-item label="衣长成衣" prop="pCoatLength">
                      <el-input type="number" min="0" v-model="measureInfo.pCoatLength" placeholder=""></el-input>
                  </el-form-item>

                  <el-form-item label="长袖长测量" prop="mSleeveLength">
                      <el-input type="number" min="30" v-model="measureInfo.mSleeveLength" placeholder=""></el-input>
                  </el-form-item>
                 <el-form-item label="长袖长成衣" prop="pSleeveLength">
                      <el-input type="number" min="0" v-model="measureInfo.pSleeveLength" placeholder=""></el-input>
                  </el-form-item>

                  <el-form-item label="臂围测量" prop="mArm">
                      <el-input type="number" min="30" v-model="measureInfo.mArm" placeholder=""></el-input>
                  </el-form-item>
                 <el-form-item label="臂围成衣" prop="pArm">
                      <el-input type="number" min="0" v-model="measureInfo.pArm" placeholder=""></el-input>
                  </el-form-item>

                  <el-form-item label="中臂围测量" prop="mMiddleArm">
                      <el-input type="number" min="30" v-model="measureInfo.mMiddleArm" placeholder=""></el-input>
                  </el-form-item>
                 <el-form-item label="中臂围成衣" prop="pMiddleArm">
                      <el-input type="number" min="0" v-model="measureInfo.pMiddleArm" placeholder=""></el-input>
                  </el-form-item>

                  <el-form-item label="腕围测量" prop="mWrist">
                      <el-input type="number" min="30" v-model="measureInfo.mWrist" placeholder=""></el-input>
                  </el-form-item>
                 <el-form-item label="腕围成衣" prop="pWrist">
                      <el-input type="number" min="0" v-model="measureInfo.pWrist" placeholder=""></el-input>
                  </el-form-item>

                  <el-form-item label="" style="display:block;text-align: center;">
                      <el-button type="primary" @click="onSubmit3">查询</el-button>
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
      form1: {
        //表单对象
        name: "",
        region: "",
        date1: "",
        date2: "",
        delivery: false,
        type: [],
        resource: "",
        desc: ""
      },
      form2: {
        //表单对象
        name: "",
        amount: "",
        region: "",
        date1: "",
        date2: "",
        delivery: false,
        type: [],
        resource: "",
        desc: ""
      },
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
      labelWidth: "100px", //lable宽度
      rules: {
        name: [
          { required: true, message: "请输入活动名称", trigger: "blur" },
          { min: 3, max: 5, message: "长度在 3 到 5 个字符", trigger: "blur" }
        ],
        amount: [{ required: true, message: "请输入金额", trigger: "blur" }],

        mNeck: [{ required: true, message: "请输入尺寸", trigger: "blur" }],
        pNeck: [{ required: true, message: "请输入尺寸", trigger: "blur" }],

        mBust: [{ required: true, message: "请输入尺寸", trigger: "blur" }],
        pBust: [{ required: true, message: "请输入尺寸", trigger: "blur" }],

        mWaist: [{ required: true, message: "请输入尺寸", trigger: "blur" }],
        pWaist: [{ required: true, message: "请输入尺寸", trigger: "blur" }],

        mBelly: [{ required: true, message: "请输入尺寸", trigger: "blur" }],
        pBelly: [{ required: true, message: "请输入尺寸", trigger: "blur" }],


        mHipline: [{ required: true, message: "请输入尺寸", trigger: "blur" }],
        pHipline: [{ required: true, message: "请输入尺寸", trigger: "blur" }],

        mShoulderLength: [{ required: true, message: "请输入尺寸", trigger: "blur" }],
        pShoulderLength: [{ required: true, message: "请输入尺寸", trigger: "blur" }],

        mCoatLength: [{ required: true, message: "请输入尺寸", trigger: "blur" }],
        pCoatLength: [{ required: true, message: "请输入尺寸", trigger: "blur" }],

        mSleeveLength: [{ required: true, message: "请输入尺寸", trigger: "blur" }],
        pSleeveLength: [{ required: true, message: "请输入尺寸", trigger: "blur" }],

        mArm: [{ required: true, message: "请输入尺寸", trigger: "blur" }],
        pArm: [{ required: true, message: "请输入尺寸", trigger: "blur" }],

        mMiddleArm: [{ required: true, message: "请输入尺寸", trigger: "blur" }],
        pMiddleArm: [{ required: true, message: "请输入尺寸", trigger: "blur" }],

        mWrist: [{ required: true, message: "请输入尺寸", trigger: "blur" }],
        pWrist: [{ required: true, message: "请输入尺寸", trigger: "blur" }],





        date1: [
          {
            type: "date",
            required: true,
            message: "请选择日期",
            trigger: "change"
          }
        ],
        date2: [
          {
            type: "date",
            required: true,
            message: "请选择时间",
            trigger: "change"
          }
        ],
        type: [
          {
            type: "array",
            required: true,
            message: "请至少选择一个活动性质",
            trigger: "change"
          }
        ],
        resource: [
          { required: true, message: "请选择活动资源", trigger: "change" }
        ],
        suitSize: [
          { required: true, message: "请选择", trigger: "change" }
        ],
        desc: [{ required: true, message: "请填写活动形式", trigger: "blur" }]
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
