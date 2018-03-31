<template>
 <!-- 热门技术 -->
  <div class="advanback" :style="{background: 'url('+advanBackBottomBg+')'}">
    <div class="threeBox">
        <el-row :gutter="30">
          <el-col :span="8" class="box" v-for="itemgh in itemArray" :key="itemgh.key">
              <div :class="itemgh.icon"></div>
              <p class="text">{{itemgh.text}}</p>
              <h6 class="htext">{{itemgh.htext}}</h6>
          </el-col>
        </el-row>
    </div>
    <div class="sixMainBox">
        <el-row :gutter="40">
          <el-col :span="8" v-for="itemsix in itemArrayMain" :key="itemsix.key">
              <div class="sixbox">
                  <i :class="itemsix.icon" class="elIcon"></i>
                  <span class="textMainHover">{{itemsix.title}}</span>
                  <h6 class="textMainHover">{{itemsix.text}}</h6>
              </div>
          </el-col>
        </el-row>
    </div>
  </div>
</template>

<script>


  export default {
    name: 'advanback',
    data() {
      return {
        advanBackBottomBg: require('../../assets/images/zhuanjiapic/advanback.jpg'),
        logoBottomBg: require('../../assets/images/zhuanjiapic/72.png'),
        itemArray : [
            {text : "课题背景" , htext :"二十一世纪以来，互联网进入了高速发展的新时代。网络逐渐在人们的生活中占有一席之地，互联网俨然已经成为人们快速获取信息、发布信息和传递信息的主要传播渠道。", key : "1", icon : "logo"},
            {text : "目的和意义" , htext :"在线问卷调查系统的目的就是能够提高调查信息的速度、范围以及准确度，并能够有效地控制节约因传统纸质版调查问卷而产生的费用和响应现今国家提倡节能减排问题。" ,key : "2", icon : "logo1"},
            {text : "国内外现状" , htext :"国内市场中，像在线问卷调查系统这种能灵活、快速、不考虑范围的获取信息咨询的网站也在逐渐增多，例如：问卷星、百度问卷等，同样存在着操作复杂、适合人群范围小等问题。", key : "3", icon : "logo2"}
        ],
        itemArrayMain : [
            {icon : "el-icon-edit" , title : "1.数据库存储" , text : "打开Visual Studio 2010后，所有有关于数据库的操作都封装在App_Code目录下的DbHelperSQL.cs类中，用时直接调用相应的方法即可。", key : "1"},
            {icon : "el-icon-document" , title : "2.主页界面的实现" , text : "主页界面是打开在线问卷调查系统的第一个界面，主页界面采用简洁清新的风格，让用户浏览时不管浏览多久都不会感觉到视觉疲劳。", key : "2"},
            {icon : "el-icon-phone-outline" , title : "3.登录界面的设计与实现" , text : "管理员登录后台管理系统界面和其他界面相比是一个较简单实现的的界面，管理员想要登录后台管理系统输入正确的“账号和密码”，后按“登录”即可登录该后台管理系统。", key : "3"},
            {icon : "el-icon-printer" , title : "4.会员注册界面的设计与实现" , text : "会员注册界面是想要回答问卷的网站浏览者的必经之路，网站的各个界面都可以随意浏览，但如果浏览者想要对问卷进行回答就需要注册成为会员。", key : "4"},
            {icon : "el-icon-service" , title : "5.会员注册界面的实现" , text : "此页面实现会员的注册，会员注册信息包括：用户名、登录密码、姓名、性别、年龄、联系方式、电子邮箱、密码保护问题、密码保护答案。红色“*”为必填写的信息，注册信息填写完点击“注册”即可。", key : "5"},
            {icon : "el-icon-success" , title : "6.问卷填写界面的设计与实现" , text : "问卷填写界面就是在线问卷调查系统的核心内容，整个系统的主要功能。开发这个在线问卷调查系统就是为了能实现问卷填写这一功能。会员注册成功后，就能体验问卷调查的强大的功能。", key : "6"},
        ]

      }
    }

  }

</script>

<style scoped>
  .advanback {
    background-size: 100%;
    height: 823px;
    margin-top: 80px;
  }
.threeBox {
    width: 1000px;
    height: 350px;
    border-bottom:1px solid #ddd;
    margin: 0 auto;
}
.box {
    padding-top: 10%;
}
.logo {
    width: 80px;
    height: 80px;
    overflow: hidden; 
    margin: 0 auto;
    z-index: 99999;
    background: url(../../assets/images/zhuanjiapic/72.png) no-repeat;
    /* border:1px solid #fff; */
    /* border-radius: 100%;     */
}
.logo1 {
    width: 80px;
    height: 80px;
    overflow: hidden; 
    margin: 0 auto;
    z-index: 99999;
    background: url(../../assets/images/zhuanjiapic/free.png) no-repeat;
    /* border:1px solid #fff; */
    /* border-radius: 100%;     */
}
.logo2 {
    width: 80px;
    height: 80px;
    overflow: hidden; 
    margin: 0 auto;
    z-index: 99999;
    background: url(../../assets/images/zhuanjiapic/low.png) no-repeat;
    /* border:1px solid #fff; */
    /* border-radius: 100%;     */
}


.text {
    color: #fff;
    font-size: 1.4em;
}
.logo:hover{
    background-position: 0 -80px;
    /* color: red; */
    /* border-width: 100px; */
    /* transition: 1s; */
}
.logo1:hover{
    background-position: 0 -80px;
    /* color: red; */
    /* border-width: 100px; */
    /* transition: 1s; */
}
.logo2:hover{
    background-position: 0 -80px;
    /* color: red; */
    /* border-width: 100px; */
    /* transition: 1s; */
}
.htext {
   color:#a6bad3;
}

.sixMainBox {
    width: 1000px;
    height: 400px;
    border-bottom:1px solid #ddd;
    margin: 0 auto;
}
.sixbox {
    padding-top: 40px;
    font-size: 1.2em;
    color: #0972d4;
    font-weight: 800;
    height: 140px;
}
.sixbox .elIcon{
    font-size: 2em;
    color: #0972d4;
}
.sixbox:hover .textMainHover{
    color: #a6bad3;
    /* font-weight: 800; */
}
</style>
