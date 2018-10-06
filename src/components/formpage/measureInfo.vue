<template >
    <div>

        横向表单:
        <!-- 查询区----start -->
        <!-- 查询区----end -->
        纵向单列表单(含验证):
        <div class="container suit_style" style="width: 660px;">
            <el-form :label-position="labelPosition" :rules="rules" ref="suit_style" :label-width="labelWidth" :inline="false" :model="suit_style" class="demo-form-inline">

                <el-form-item label="纽扣颜色" prop="fastenerColor">
                    <el-radio-group v-model="suit_style.fastenerColor">
                        <el-radio label="白色"></el-radio>
                        <el-radio label="黑色"></el-radio>
                    </el-radio-group>
                </el-form-item>
                <el-form-item label="工艺选择" prop="processSeletion" >
                    <el-input v-model="suit_style.processSeletion" placeholder="工艺选择" value="男式1.0"></el-input>
                </el-form-item>
                <el-form-item label="衬衫面料" prop="suitType">
                    <el-input v-model="suit_style.suitType" placeholder="衬衫面料"></el-input>
                </el-form-item>
                <!-- <el-form-item label="数字框" prop="amount">
                    <el-input type="number" min="0" v-model="form2.amount" placeholder="金额"></el-input>
                </el-form-item> -->
                <el-form-item label="领型选择" prop="collarType">
                    <el-select v-model="suit_style.collarType" placeholder="领型">
                        <el-option label="温莎领" value="温莎领"></el-option>
                        <el-option label="标准领" value="标准领"></el-option>
                        <el-option label="中八领" value="中八领"></el-option>
                    </el-select>
                </el-form-item>
                <el-form-item label="袖型选择" prop="cuffType">
                    <el-select v-model="suit_style.cuffType" placeholder="领型">
                        <el-option label="斜角单扣" value="斜角单扣"></el-option>
                        <el-option label="圆角单扣" value="圆角单扣"></el-option>
                        <el-option label="斜角双扣" value="斜角双扣"></el-option>
                    </el-select>
                </el-form-item>
                <el-form-item label="门襟选择" prop="topFly">
                    <el-select v-model="suit_style.topFly" placeholder="门襟">
                        <el-option label="明门襟" value="明门襟"></el-option>
                        <el-option label="翻门襟" value="翻门襟"></el-option>
                    </el-select>
                </el-form-item>
                <el-form-item label="下摆选择" prop="Hem">
                    <el-select v-model="suit_style.Hem" placeholder="下摆">
                        <el-option label="圆摆" value="圆摆"></el-option>
                        <el-option label="平摆" value="平摆"></el-option>
                    </el-select>
                </el-form-item>
                <el-form-item label="收省" prop="collectSuit">
                    <el-select v-model="suit_style.collectSuit" placeholder="收省">
                        <el-option label="正常" value="正常"></el-option>
                        <el-option label="双肩活折" value="双肩活折"></el-option>
                        <el-option label="后腰省" value="后腰省"></el-option>
                    </el-select>
                </el-form-item>
                <el-form-item label="领口颜色" prop="collarColor">
                    <el-radio-group v-model="suit_style.collarColor">
                        <el-radio label="同身"></el-radio>
                        <el-radio label="白色撞领袖"></el-radio>
                    </el-radio-group>
                </el-form-item>
                <el-form-item label="口袋选择" prop="isPocket">
                    <el-radio-group v-model="suit_style.isPocket">
                        <el-radio label="无口袋"></el-radio>
                        <el-radio label="有口袋"></el-radio>
                    </el-radio-group>
                </el-form-item>
                <el-form-item label="纽扣选择" prop="fastenerType">
                    <el-radio-group v-model="suit_style.fastenerType">
                        <el-radio label="普通纽扣"></el-radio>
                        <el-radio label="贝壳纽扣"></el-radio>
                    </el-radio-group>
                </el-form-item>
                <el-form-item label="纽扣颜色" prop="fastenerColor">
                    <el-radio-group v-model="suit_style.fastenerColor">
                        <el-radio label="白色"></el-radio>
                        <el-radio label="黑色"></el-radio>
                    </el-radio-group>
                </el-form-item>



                <!-- <el-form-item label="活动时间" prop="date1">
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
                <el-form-item label="单选按钮" prop="suitSize">
                    <el-radio-group v-model="suit_style.suitSize">
                        <el-radio label="线上品牌商赞助"></el-radio>
                        <el-radio label="线下场地免费"></el-radio>
                    </el-radio-group>
                </el-form-item>
                <el-form-item label="文本域" prop="desc">
                    <el-input type="textarea" v-model="form2.desc"></el-input>
                </el-form-item> -->
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
      labelWidth: "80px", //lable宽度
      rules: {
        name: [
          { required: true, message: "请输入活动名称", trigger: "blur" },
          { min: 3, max: 5, message: "长度在 3 到 5 个字符", trigger: "blur" }
        ],
        amount: [{ required: true, message: "请输入金额", trigger: "blur" }],

        suitType: [{ required: true, message: "请输入衬衫面料", trigger: "blur" }],
        processSeletion: [{ required: true, message: "请输入衬衫规格", trigger: "blur" }],
        collarType: [
          { required: true, message: "请选择领型", trigger: "change" }
        ],
        cuffType: [
          { required: true, message: "请选择袖型", trigger: "change" }
        ],
        topFly: [
          { required: true, message: "请选择门襟", trigger: "change" }
        ],
        Hem: [
          { required: true, message: "请选择下摆", trigger: "change" }
        ],
        collectSuit: [
          { required: true, message: "请选择收省", trigger: "change" }
        ],
        collarColor: [
          { required: true, message: "请选择领口颜色", trigger: "change" }
        ],
        isPocket: [
          { required: true, message: "请选择口袋", trigger: "change" }
        ],
        fastenerType: [
          { required: true, message: "请选择纽扣", trigger: "change" }
        ],
        fastenerColor: [
          { required: true, message: "请选择纽扣颜色", trigger: "change" }
        ],

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
