<!-- 个人信息 -->
<template>
  <div>
    <h2>目前薪资</h2>
    <el-form>
      <el-form-item label="薪资总计约">
        <el-input v-model="profile.payTotal" placeholder="请输入薪资总计"></el-input>
      </el-form-item>
      <el-form-item label="基本薪资">
        <el-input v-model="profile.jbPay" placeholder="请输入基本薪资"></el-input>
      </el-form-item>
      <el-form-item label="绩效薪资">
        <el-input v-model="profile.jxPay" placeholder="绩效薪资"></el-input>
      </el-form-item>
      <el-form-item label="管理津贴">
        <el-input v-model="profile.gljt" placeholder="请输入管理津贴"></el-input>
      </el-form-item>
      <el-form-item label="交通津贴">
        <el-input v-model="profile.jtjt" placeholder="请输入交通津贴"></el-input>
      </el-form-item>
      <el-form-item label="餐饮津贴">
        <el-input v-model="profile.cyjt" placeholder="餐饮津贴"></el-input>
      </el-form-item>
      <el-form-item label="住宿津贴">
        <el-input v-model="profile.zsjt" placeholder="住宿津贴"></el-input>
      </el-form-item>
      <el-form-item label="年终奖">
        <el-input v-model="profile.nzj" placeholder="年终奖"></el-input>
      </el-form-item>

      <el-form-item label="备注">
        <el-input v-model="profile.remark" placeholder="备注"></el-input>
      </el-form-item>


    </el-form>
  </div>
</template>

<script>
  // import Imges from './Imges.vue'
  export default {
    props: ['profile'],
    // components: {
    //   Imges
    // }
  }
</script>



