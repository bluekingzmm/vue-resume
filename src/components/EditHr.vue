<!-- 个人信息 -->
<template>
  <div>
    <h2>hr</h2>
    <el-form>
      <el-form-item label="日期">
        <el-input v-model="profile.date" placeholder="请输入日期"></el-input>
      </el-form-item>
      <el-form-item label="公司名称及类型">
        <el-input v-model="profile.companyType" placeholder="请输入公司名称及类型"></el-input>
      </el-form-item>
      <el-form-item label="职位名称">
        <el-input v-model="profile.positionName" placeholder="职位名称"></el-input>
      </el-form-item>
      <el-form-item label="人力资源窗口">
        <el-input v-model="profile.hrzy" placeholder="请输入人力资源窗口"></el-input>
      </el-form-item>
      <el-form-item label="公司客户窗口">
        <el-input v-model="profile.companykh" placeholder="请输入客户窗口"></el-input>
      </el-form-item>
      <el-form-item label="顾问联系方式">
        <el-input v-model="profile.gwPhone" placeholder="顾问联系方式"></el-input>
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



