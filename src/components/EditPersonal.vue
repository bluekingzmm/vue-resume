<!-- 个人信息 -->
<template>
  <div>
    <h2>个人信息</h2>
    <el-form>
      <el-form-item label="姓名">
        <el-input v-model="profile.name" placeholder="请输入姓名"></el-input>
      </el-form-item>

      <el-form-item label="出生日期">
        <el-input v-model="profile.birthdate" placeholder="请输入出生日期"></el-input>
      </el-form-item>
      <el-form-item label="性别">
        <el-input v-model="profile.sex" placeholder="请输入性别"></el-input>
      </el-form-item>

      <el-form-item label="国际地区">
        <el-input v-model="profile.area" placeholder="请输入国际地区"></el-input>
      </el-form-item>
      <el-form-item label="婚姻状况">
        <el-input v-model="profile.maritalStatus" placeholder="请输入婚姻状况"></el-input>
      </el-form-item>
      <el-form-item label="目前所在地">
        <el-input v-model="profile.city" placeholder="请输入目前所在地"></el-input>
      </el-form-item>
      <el-form-item label="联系电话">
        <el-input v-model="profile.phone" placeholder="请输入联系电话"></el-input>
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



