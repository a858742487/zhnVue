<template>
  <!-- 政策计划 -->
  <div class="policyIndex">
    <!-- <policyBanner></policyBanner> -->
    <el-card class="box-card">
      <div class="indexMainBox">
        <h2>会员注册</h2>
        <el-form :model="ruleForm" :rules="rules" ref="ruleForm" label-width="100px" class="demo-ruleForm">
          <el-form-item label="账号" prop="name">
            <el-input v-model="ruleForm.name"></el-input>
          </el-form-item>
          <el-form-item label="密码" prop="mima">
            <el-input v-model="ruleForm.mima"></el-input>
          </el-form-item>
          <el-form-item label="确认密码" prop="mimaMini">
            <el-input v-model="ruleForm.mimaMini"></el-input>
          </el-form-item>
          <el-form-item label="手机号码" prop="iPhone">
            <el-input v-model="ruleForm.iPhone"></el-input>
          </el-form-item>
          <el-form-item label="邮箱地址" prop="mail">
            <el-input v-model="ruleForm.mail"></el-input>
          </el-form-item>
          <el-form-item>
            <el-button type="primary" @click="onSubmit()">立即注册</el-button>
          </el-form-item>
        </el-form>
      </div>
    </el-card>
  </div>
</template>

<script>
  //   import zhuanjiaBanner from './zhuanjiaMain/zhuanjiaBanner'
  import policyBanner from './policyBanner'
  export default {
    name: 'policyIndex',
    data() {
      return {
        currentDate: new Date(),
        tableData: [],
         ruleForm: {
          name: '',
          mima: '',
          mimaMini : '',
          iPhone : '',
          mail : '',
        },
        rules: {
          name: [
            { required: true, message: '请输入账号', trigger: 'blur' },
            { min: 3, max: 15, message: '长度在 3 到 15 个字符', trigger: 'blur' }
          ],
          mima: [
            { required: true, message: '请输入密码', trigger: 'blur' },
            { min: 3, max: 15, message: '长度在 3 到 15 个字符', trigger: 'blur' }
          ],
          mimaMini: [
            { required: true, message: '请输入正确密码', trigger: 'blur' },
            { min: 3, max: 15, message: '长度在 3 到 15 个字符', trigger: 'blur' }
          ],
          iPhone : [
            { required: true, message: '请输入手机号码', trigger: 'blur' },
            { min: 11, max: 11, message: '长度在 11 个字符', trigger: 'blur' }
          ],
          mail : [
            { required: true, message: '请输入手机号码', trigger: 'blur' }
          ]
        }
      }
    },
    components: {
      policyBanner
    },
    methods: {
      onSubmit() {
        alert('注册成功');
      }
    },
    created() {
      this.$http.get(
        'https://bird.ioliu.cn/v1?url=http://120.76.205.241:8000/news/qihoo?kw=%E4%B8%93%E5%AE%B6&site=http%3A%2F%2Fnews.sohu.com%2F&apikey=PXYYZZLJn5JSfTasvTJUai1bIjyQNT9g6rsPg2LXUWf44KimzdnXEamLhqJdVpLb', {
          params: {
  
          }
        }).then(res => {
        this.tableData = res.data.data;
        // console.log(this.tableData[0].create_at);
      }, response => {
        console.log("res");
      })
    }
  }
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  .text {
    font-size: 14px;
  }
  
  .item {
    margin-bottom: 18px;
  }
  
  .clearfix:before,
  .clearfix:after {
    display: table;
    content: "";
  }
  
  .clearfix:after {
    clear: both
  }
  
  .box-card {
    width: 600px;
    margin: 0 auto;
    margin-top: 50px;
    margin-bottom: 100px;
  }
  
  .indexMainBox {
    width: 500px;
    margin: 0 auto;
    /* border: 1px solid #ddd; */
    /* height: 200px; */
  }
  
  .time {
    font-size: 13px;
    color: #999;
  }
  
  .bottom {
    margin-top: 13px;
    line-height: 12px;
  }
  
  .button {
    padding: 0;
    float: right;
  }
  
  .image {
    width: 100%;
    display: block;
  }
  
  .clearfix:before,
  .clearfix:after {
    display: table;
    content: "";
  }
  
  .clearfix:after {
    clear: both
  }
  
  .listPolicy {
    margin: 20px;
  }
  
  .policyBottomPic {
    width: 1000px;
    margin: 40px 0 50px 0;
  }
  
  .policyBottomPic img {
    width: 100%;
    height: 200px;
  }
  
  .policyImg .image {
    height: 300px;
  }
  
  .policyBottomPic .title {
    text-align: left;
  }
  
  .titleSpan {
    display: -webkit-box;
    -webkit-box-orient: vertical;
    -webkit-line-clamp: 1;
    overflow: hidden;
  }
</style>
