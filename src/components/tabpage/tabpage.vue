<template>
    <div>
        <div class="pagepath">

        </div>
        <!-- <el-breadcrumb separator="/" style="padding:10px;border:1px solid #ddd;background:#fff;margin-bottom:1px;">
            <el-breadcrumb-item :to="{ path: '/' }">首页</el-breadcrumb-item>
            <el-breadcrumb-item>
                <a href="/">活动管理</a>
            </el-breadcrumb-item>
            <el-breadcrumb-item>活动列表</el-breadcrumb-item>
            <el-breadcrumb-item>活动详情</el-breadcrumb-item>
        </el-breadcrumb> -->
        <!-- <el-tabs v-model="activeName" @tab-click="handleClick">
          <el-tab-pane label="用户管理" name="first">用户管理</el-tab-pane>
          <el-tab-pane label="配置管理" name="second">配置管理</el-tab-pane>
          <el-tab-pane label="角色管理" name="third">角色管理</el-tab-pane>
          <el-tab-pane label="定时任务补偿" name="fourth">定时任务补偿</el-tab-pane>
        </el-tabs>
        <button @click="change()">asda</button> -->

        <el-tabs  v-model="activeName" type="border-card">
            <el-tab-pane label="款式搭配" >
                <formpage @changeTab="getTab"></formpage>
                <!-- <v-searchinput></v-searchinput> -->
            </el-tab-pane>
            <el-tab-pane label="量体数据" >
                <measureInfo></measureInfo>
            </el-tab-pane>
            <el-tab-pane label="特体数据（非必填）">角色管理</el-tab-pane>
            <el-tab-pane label="刺绣内容">
              <stitchwork></stitchwork>
            </el-tab-pane>
            <el-tab-pane label="客户信息">
              <customerInfo></customerInfo>
            </el-tab-pane>
        </el-tabs>

    </div>
</template>
<style>

</style>

<script>
import vSearchinput from '../searchinput/searchinput.vue';
import formpage from '../formpage/formpage.vue';
import measureInfo from '../formpage/measureInfo.vue';
import stitchwork from '../formpage/stitchwork.vue';
import customerInfo from '../formpage/customerInfo.vue';
export default {
    name: 'tabpage',
    components: {
        vSearchinput,
        formpage,
        stitchwork,
        customerInfo,
        measureInfo
    },
    data() {
      return {
        activeName: 0,
      };
    },
    methods: {
      handleClick(tab, event) {
        // console.log(tab, event);
        console.log(this.activeName);
      },
      change(){
        this.activeName = 'third';
      },
      getTab(msg){
        this.activeName = msg;
        console.log("success",msg);
      }
    }
}
</script>
