<template>
  <!-- 首页专家技术热门轮播 技术热门 -->
  <div class="hotTechnology">
    <el-container>
      <el-header>
        <div class="titleName">
          问卷调查
        </div>
      </el-header>
      <el-container>
        <el-aside width="500px" class="leftNameColor">
          <el-card class="box-card">
            <div slot="header" class="clearfix">
              <span>最新问卷</span>
              <!-- <el-button style="float: right; padding: 3px 0" type="text">操作按钮</el-button> -->
            </div>
            <div v-for="o in 9" :key="o" class="text item textLeft textLeftHight">
              <router-link to="item.link">
                <span class='textLeft'>{{o+'.'+' 调查列表'}}</span>
                <span class='textright'>2018-3-30</span>
              </router-link>
            </div>
          </el-card>1
        </el-aside>
        <el-aside width="500px" class="leftNameColor">
          <el-card class="box-card">
            <div slot="header" class="clearfix">
              <span>网站公告</span>
              <!-- <el-button style="float: right; padding: 3px 0" type="text">操作按钮</el-button> -->
            </div>
            <div v-for="o in 9" :key="o" class="text item textLeft textLeftHight">
              <router-link to="item.link">
                <span class='textLeft'>{{o+'.'+' 调查列表'}}</span>
                <span class='textright'>2018-3-30</span>
              </router-link>
            </div>
          </el-card>1
        </el-aside>
        <!-- <el-main class="border">Main</el-main> -->
      </el-container>
    </el-container>
  </div>
</template>

<script>
  export default {
    name: 'hotTechnology',
    data() {
      return {
        indexThreepic: []
      }
    },
    methods: {
  
    },
    created() {
      // var url = 
      this.$http.get(
        'https://bird.ioliu.cn/v1?url=http://120.76.205.241:8000/news/qihoo?kw=n&site=qq.com&apikey=PXYYZZLJn5JSfTasvTJUai1bIjyQNT9g6rsPg2LXUWf44KimzdnXEamLhqJdVpLb', {
          params: {
  
          }
        }).then(res => {
        this.indexThreepic = res.data.data;
        // console.log(this.tableData[0].create_at);
  
      }, response => {
        console.log("res");
      })
    }
  }
</script>

<style scoped>
  .hotTechnology {
    padding-top: 2%;
    width: 1000px;
  }
  
  .el-carousel__item h3 {
    color: #475669;
    font-size: 14px;
    opacity: 0.75;
    line-height: 200px;
    margin: 0;
  }
  
  .el-carousel__item:nth-child(2n) {
    background-color: #fff;
  }
  
  .el-carousel__item:nth-child(2n+1) {
    background-color: #fff;
  }
  
  .threepicimg {
    width: 550px;
    height: 260px;
    margin: 0;
    padding: 0;
    /* margin-bottom: 300px;  */
  }
  
  .threeboxwidth {
    /* width: 445px !important; */
    padding-top: 20px;
    border-radius: 5px;
    /* margin-bottom: 300px;  */
  }
  
  .leftNameColor {
    color: #fff;
  }
  
  .titlehot {
    color: #fff;
    font-family: "黑体";
    padding-bottom: 2%;
    font-size: 2em;
    letter-spacing: 10px;
    font-weight: 800;
  }
  
  .titleName {
    color: #000;
    font-size: 30px;
  }
  
  .textLeft {
    text-align: left;
  }
  .textLeft:hover {
    color: #0972d4;
  }
  .textright {
    float: right;
    padding-right: 20px;
  }
  
  .textLeftHight {
    line-height: 40px;
  }
  
  .border {
    border: 1px solid #ddd;
  }
</style>
