<template>
<!-- 首页number -->
  <div class="numberIndex" :style="{background: 'url('+bglan+')'}">
    <div class="main">
      <el-row>
        <el-col :span="8" v-for="itemnumber in inemArraynumber" :key="itemnumber.key">
          <p class="title">
            <span>{{itemnumber.munber}}</span>
          </p>
          <p class="text">{{itemnumber.text}}</p>
        </el-col>
      </el-row>
      <a href="#">
        <div class="root">查看问卷</div>
      </a>
    </div>
  </div>
</template>
<script>
  // import mainBg from '../../assets/images/banner.jpg'
  export default {
    name: 'numberIndex',
    data() {
      return {
        bglan : require('../../assets/images/banner.jpg'),
        inemArraynumber: [{
            key: "1",
            munber: "50 +个",
            text: "文件调查"
          },
          {
            key: "2",
            munber: "596 人",
            text: "累计调查人次"
          },
          {
            key: "3",
            munber: "3580 +次",
            text: "网站浏览"
          }
        ]
      }
    },
    methods: {

    }
  }

</script>

<style scoped>
  .numberIndex {
    width: 100%;
    /* border:1px solid #ddd; */
    height: 300px;
    /* margin-top: 70px; */
    background: #ddd;
    /* background: url(../../assets/images/banner.jpg); */
  }

  .main {
    width: 1000px;
    height: 300px;
    /* border: 1px solid #000; */
    margin: 0 auto;
  }

  .text {
    font-size: 0.8em;
    color:#fff;
  }

  .title {
    font-size: 2.7em;
    margin: 70px 0 0 0;
    color:#fff;
  }

  .root {
    width: 200px;
    height: 30px;
    border:1px solid #000;
    margin: 0 auto;
    line-height:30px;
    margin-top:50px;
    border-radius: 5px;
    font-weight:800;
    color:#fff;

  }
  .root:hover {
    background:red;
    color:#fff;
    border:1px solid red;

  }

</style>
