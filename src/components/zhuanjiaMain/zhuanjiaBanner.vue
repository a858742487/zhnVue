<template>
  <!-- 这个页面是专家的banner -->
  <div class="zhuanjiaBanner">
    <div class="block">
      <el-card class="box-card">
  
        <el-container>
          <el-header>
            <div class="title">
              关于消费者维权调查
            </div>
          </el-header>
          <el-main>
            <el-row :gutter="20">
              <el-col :span="12" :offset="12">
                <div class="grid-content bg-purple">作者：admin 发布时间：2018-03-09 18:26:44 浏览量：1677</div>
              </el-col>
              <div class="ListLiBox">
                <div>
                  1.您的性别
                </div>
                <div>
                  <el-radio v-model="radio7" label="1">男</el-radio>
                  <el-radio v-model="radio7" label="2">女</el-radio>
                </div>
              </div>
              <div class="ListLiBox">
                <div>
                  2.您的学历
                </div>
                <div>
                  <el-radio v-model="radio8" label="1">没有受过正式教育</el-radio>
                  <el-radio v-model="radio8" label="2">小学</el-radio>
                  <el-radio v-model="radio8" label="3">初中</el-radio>
                  <el-radio v-model="radio8" label="4">高中</el-radio>
                  <el-radio v-model="radio8" label="5">中专/技校</el-radio>
                  <el-radio v-model="radio8" label="6">大专或大学非本科</el-radio>
                  <el-radio v-model="radio8" label="7">本科</el-radio>
                </div>
              </div>
              <div class="ListLiBox">
                <div>
                  3.您目前的婚姻状况
                </div>
                <div>
                  <el-radio v-model="radio9" label="1">未婚</el-radio>
                  <el-radio v-model="radio9" label="2">已婚</el-radio>
                  <el-radio v-model="radio9" label="3">同居</el-radio>
                  <el-radio v-model="radio9" label="4">离异或丧偶</el-radio>
                </div>
              </div>
              <div class="ListLiBox">
                <div>
                  4.您目前所从事的职业
                </div>
                <div>
                  <el-radio v-model="radio10" label="1">国家机关/政党机关和社会团体</el-radio>
                  <el-radio v-model="radio10" label="4">计算机IT业</el-radio>
                  <el-radio v-model="radio10" label="5">房地产业</el-radio>
                  <el-radio v-model="radio10" label="6">汽车业</el-radio>
                  <el-radio v-model="radio10" label="7">学生</el-radio>
                </div>
              </div>
              <div class="ListLiBox">
                <div>
                  5. 您个人税前月总收入
                </div>
                <div>
                  <el-radio v-model="radio1" label="1">1000元以下</el-radio>
                  <el-radio v-model="radio1" label="2">1000-1999元</el-radio>
                  <el-radio v-model="radio1" label="3">2000-2999元</el-radio>
                  <el-radio v-model="radio1" label="4">3000-4999元</el-radio>
                  <el-radio v-model="radio1" label="5">5000-7999元</el-radio>
                  <el-radio v-model="radio1" label="6">8000-9999元</el-radio>
                </div>
              </div>
              <div class="ListLiBox">
                <div>
                  6. 您家庭税前月总收入
                </div>
                <div>
                  <el-radio v-model="radio2" label="1">1000元以下</el-radio>
                  <el-radio v-model="radio2" label="2">1000-1999元</el-radio>
                  <el-radio v-model="radio2" label="3">2000-2999元</el-radio>
                  <el-radio v-model="radio2" label="4">3000-4999元</el-radio>
                  <el-radio v-model="radio2" label="5">5000-7999元</el-radio>
                  <el-radio v-model="radio2" label="6">8000-9999元</el-radio>
                </div>
              </div>
              <div class="ListLiBox">
                <div>
                  7. 您的居住地址
                </div>
                <div>
                  <el-input v-model="radio3" placeholder=""></el-input>
                </div>
              </div>
              <div class="ListLiBox">
                <div>
                  8. 下列哪些方式会吸引您进入店铺？
                </div>
                <div>
                  <el-radio v-model="radio4" label="1">店铺别致的装修及形象</el-radio>
                  <el-radio v-model="radio4" label="2">店铺橱窗摆放的热销商品</el-radio>
                  <el-radio v-model="radio4" label="3">优惠促销的海报</el-radio>
                  <el-radio v-model="radio4" label="4">派发到家里的商品目录单</el-radio>
                  <el-radio v-model="radio4" label="5">店铺里面人潮涌动</el-radio>
                  <el-radio v-model="radio4" label="6">其他</el-radio>
                </div>
              </div>
              <div class="ListLiBox">
                <div>
                  9. 什么因素会影响您在网上购物
                </div>
                <div>
                  <el-radio v-model="radio5" label="1">付费安全性</el-radio>
                  <el-radio v-model="radio5" label="2">商品质量</el-radio>
                  <el-radio v-model="radio5" label="3">售后保障</el-radio>
                  <el-radio v-model="radio5" label="4">运输安全</el-radio>
                  <el-radio v-model="radio5" label="5">价格优势</el-radio>
                </div>
              </div>
              <div class="ListLiBox">
                <div>
                  10.您更愿意通过网络购买哪类商品
                </div>
                <div>
                  <el-radio v-model="radio6" label="1">数码、家电</el-radio>
                  <el-radio v-model="radio6" label="2">汽车用品、户外运动用品</el-radio>
                  <el-radio v-model="radio6" label="3">母婴用品</el-radio>
                  <el-radio v-model="radio6" label="4">化妆品</el-radio>
                  <el-radio v-model="radio6" label="5"> 服饰包包类商品</el-radio>
                </div>
              </div>
              <el-row>
                 <el-button type="primary">提交问卷</el-button>
              </el-row>
            </el-row>
          </el-main>
        </el-container>
      </el-card>
    </div>
  </div>
</template>

<script>
  export default {
    name: 'zhuanjiaBanner',
    data() {
      return {
        value4: '',
        radio1: '1',
        radio2: '1',
        radio3: '',
        radio4: '1',
        radio5: '1',
        radio6: '1',
        radio7: '1',
        radio8: '1',
        radio9: '1',
        radio10: '1',
        input: '',
        tableData: '',
        bottomBg: require('@/assets/images/zhuanjiaBanner.jpg')
      }
    },
    created() {
      this.$http.get('https://cnodejs.org/api/v1/topics', {
        params: {
          page: 1,
          limit: 5
        }
      }).then(res => {
        this.tableData = res.data.data;
        console.log(this.tableData[0].create_at);
      }, response => {
        console.log("res");
      })
    },
    methods: {
      bannersearchbtn() {
        if (this.input == '') {
          this.$message({
            message: '不能是空的哦，输入你要查询的内容吧',
            type: 'warning'
          })
        } else {
          console.log(this.input);
        }
      }
    }
  }
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  .ListLiBox {
    margin: 10px 0 10px 0;
    text-align: left;
    line-height: 30px;
    border-bottom: 1px solid #ddd;
    padding-bottom: 10px;
  }
  .el-row {
    margin-top: 40px;
  }
  .el-carousel {
    /* background: url(../assets/images/banner.jpg) */
  }
  
  .el-carousel__item h3 {
    color: #475669;
    font-size: 5em;
    opacity: 0.75;
    line-height: 50px;
    margin: 0;
  }
  
  
  /* .el-carousel__item:nth-child(2n) {
                                    background-color: #99a9bf;
                                  }
                                
                                  .el-carousel__item:nth-child(2n+1) {
                                    background-color: #d3dce6;
                                  } */
  
  .bannerSelectInput {
    width: 45%;
    height: 70px;
    border: 1px solid rgb(218, 218, 218);
    border-radius: 5px;
    position: relative;
    top: 60%;
    left: 25%;
    z-index: 3;
    /* banner上面的input */
    padding-top: 30px;
    padding-left: 100px;
    background-color: rgba(0, 0, 0, 0.3);
  }
  
  .bannerText {
    padding-top: 6%;
    height: 250px !important;
  }
  
  .bannerText h3 {
    color: #fff;
    font-size: 4em;
  }
  
  .bor {
    border-radius: 0 !important;
  }
  
  .text {
    font-size: 14px;
  }
  
  .item {
    padding: 18px 0;
  }
  
  .box-card {
    width: 1000px;
    margin: 0 auto;
  }
  
  .box-card .title {
    margin: 20px 0 20px 0;
    font-size: 30px;
    color: #5babfa;
    text-align: center;
  }
  
  .box-card .grid-content {
    font-size: 14px;
    color: #999;
  }
</style>
