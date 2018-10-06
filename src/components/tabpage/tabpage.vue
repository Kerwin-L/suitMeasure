<template>
    <div>
        <div class="pagepath">

        </div>
        <el-breadcrumb separator="/" style="padding:10px;border:1px solid #ddd;background:#fff;margin-bottom:1px;">
            <el-breadcrumb-item :to="{ path: '/' }">首页</el-breadcrumb-item>
            <el-breadcrumb-item>
                <a href="/">活动管理</a>
            </el-breadcrumb-item>
            <el-breadcrumb-item>活动列表</el-breadcrumb-item>
            <el-breadcrumb-item>活动详情</el-breadcrumb-item>
        </el-breadcrumb>

        <el-tabs type="border-card">
            <el-tab-pane label="款式搭配">
                <formpage></formpage>
                <!-- <v-searchinput></v-searchinput> -->
            </el-tab-pane>
            <el-tab-pane label="量体数据">
                <measureInfo></measureInfo>
            </el-tab-pane>
            <el-tab-pane label="特体数据（非必填）">角色管理</el-tab-pane>
            <el-tab-pane label="刺绣内容">定时任务补偿</el-tab-pane>
            <el-tab-pane label="客户信息">定时任务补偿</el-tab-pane>
        </el-tabs>

    </div>
</template>
<style>

</style>

<script>
import vSearchinput from '../searchinput/searchinput.vue';
import formpage from '../formpage/formpage.vue';
import measureInfo from '../formpage/measureInfo.vue';
export default {
    name: 'tabpage',
    components: {
        vSearchinput,
        formpage,
    },
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
            fastener:"",//纽扣选择
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
        }
    },
    methods: {

    }
}
</script>
