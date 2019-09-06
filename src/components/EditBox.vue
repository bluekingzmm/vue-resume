<template>
  <div id="EditBox">
    <nav>
      <ol>
        <li v-bind:class="{active: currentTab === 0}" v-on:click="currentTab = 0 ">
          <svg class="icon">
            <use xlink:href="#icon-fon1"></use>
          </svg>
          <p>Hr</p>
        </li>

        <li v-bind:class="{active: currentTab === 1}" v-on:click="currentTab = 1 ">
          <svg class="icon">
            <use xlink:href="#icon-fon1"></use>
          </svg>
          <p>基本信息</p>
        </li>

        <li v-bind:class="{active: currentTab === 2}" v-on:click="currentTab = 2 ">
          <svg class="icon">
            <use xlink:href="#icon-fon4"></use>
          </svg>
          <p>教育背景</p>
        </li>

        <li v-bind:class="{active: currentTab === 3}" v-on:click="currentTab = 3 ">
          <svg class="icon">
            <use xlink:href="#icon-fon5"></use>
          </svg>
          <p>专业证照</p>
        </li>


        <li v-bind:class="{active: currentTab === 4}" v-on:click="currentTab = 4 ">
          <svg class="icon">
            <use xlink:href="#icon-fon5"></use>
          </svg>
          <p>目前薪资</p>
        </li>

        <li v-bind:class="{active: currentTab === 5}" v-on:click="currentTab = 5 ">
          <svg class="icon">
            <use xlink:href="#icon-fon2"></use>
          </svg>
          <p>职业经历</p>
        </li>

        <li v-bind:class="{active: currentTab === 6}" v-on:click="currentTab = 6 ">
          <svg class="icon">
            <use xlink:href="#icon-fon3"></use>
          </svg>
          <p>项目经历</p>
        </li>


      </ol>
    </nav>
    <ol class="write">
      <!-- <li v-for = "i in  [0,1,2,3,4,5]"  v-bind:class = "{active: currentTab === i}" >
                            tab{{i + 1}}
                          </li> -->
      <li v-bind:class="{active: currentTab === 0}">
        <EditHr v-bind:profile="resume.hr"/>
      </li>

      <li v-bind:class="{active: currentTab === 1}">
        <EditPersonal v-bind:profile="resume.profile"/>
      </li>


      <li v-bind:class="{active: currentTab === 2}">
        <EditWork v-bind:workExperience="resume.education" v-bind:labels="{time:'时间',school:'学校',degree:'学历'}"
                  title="教育背景"/>
        <!-- <EditEducation v-bind:education="education" /> -->
      </li>

      <li v-bind:class="{active: currentTab === 3}">
        <EditWork v-bind:workExperience="resume.award" v-bind:labels="{name:'证照',time:'时间'}" title="专业证照"/>
      </li>


      <li v-bind:class="{active: currentTab === 4}">
        <EditPay v-bind:profile="resume.pay"/>
      </li>

      <li v-bind:class="{active: currentTab === 5}">
        <EditWork v-bind:workExperience="resume.work"
                  v-bind:labels="{company:'公司名称',date:'工作时间',introduce:'公司介绍',position:'职务',content:'工作内容',lzyy:'离职原因',xsrs:'下属人数',hbdx:'汇报对象'}"
                  title="职业经历"/>
      </li>

      <li v-bind:class="{active: currentTab === 6}">
        <EditWork v-bind:workExperience="resume.project"
                  v-bind:labels="{name:'项目名称',introduce:'项目介绍',yj:'工作业绩',date:'项目时间',position:'项目职务',content:'工作内容'}"
                  title="项目经历"/>
      </li>
      <!--<li v-bind:class="{active: currentTab === 6}">-->
      <!--<h2>联系方式</h2>-->
      <!--<el-form>-->
      <!--<el-form-item label="手机">-->
      <!--<el-input v-model="resume.contact.mobile" placeholder="请输入手机"></el-input>-->
      <!--</el-form-item>-->
      <!--<el-form-item label="微信">-->
      <!--<el-input v-model="resume.contact.WeChat" placeholder="请输入手机"></el-input>-->
      <!--</el-form-item>-->
      <!--<el-form-item label="博客">-->
      <!--<el-input v-model="resume.contact.blogger" placeholder="请输入微信"></el-input>-->
      <!--</el-form-item>-->
      <!--<el-form-item label="邮箱">-->
      <!--<el-input v-model="resume.contact.email" placeholder="请输入邮箱"></el-input>-->
      <!--</el-form-item>-->
      <!--</el-form>-->
      <!--</li>-->
    </ol>
  </div>
</template>

<script>
  import EditHr from "./EditHr";
  import EditPersonal from "./EditPersonal";
  import EditWork from "./EditWork";
  import EditPay from "./EditPay";

  export default {
    components: {
      EditHr,
      EditPersonal,
      EditWork,
      EditPay
      // EditEducation,
    },
    props: ["resume"],
    data() {
      return {
        currentTab: 0
      };
    }
  };
</script>

<style lang="scss">
  #EditBox {
    display: flex;

  > nav {
    width: 90px;
    background: #2e7b87;
    background: #409EFF;

  > ol > li {
    color: #fff;
    text-align: center;
    padding: 16px;
  }

  &
  .active {
    background: #fff;

  > p {
    color: #000;
  }

  > .icon {
    fill: #000;
  }

  }
  }
  > .write {
    overflow: hidden;
    flex: 1;

  .useless {
    position: relative;

  > .el-icon-delete {
    position: absolute;
    right: 0;
    top: 12px;
  }

  }
  > li {
    display: none;
    padding: 32px;
    height: 100%;
    overflow: auto;
  }

  &
  .active {
    display: block;
  }

  }
  }
</style>
