<template>
  <div id="app">
    <el-container>
      <el-header class="header-box">
        <el-row class="container">
          <el-col :span="8">
            <div class="logo">
            校园云生活平台
            </div>
          </el-col>
          <el-col :span="8">
            <el-form :inline="true" :model="form" class="demo-form-inline">
              <el-form-item>
                <el-input v-model="form.search" placeholder="输入搜索内容"></el-input>
              </el-form-item>
              <el-form-item>
                <el-button type="primary">搜索</el-button>
              </el-form-item>
            </el-form>
          </el-col>
          <el-col :span="8">
            <div class="">
            <el-row class="user-block">
              <el-button type="info">注册</el-button>
              <el-button>登录</el-button>
            </el-row>
            </div>
          </el-col>
        </el-row>
        <el-row>

        </el-row>
      </el-header>
      <el-main>
        <router-view/>
      </el-main>
      <el-footer class="layout-footer" style="padding: 0;">
        <div class="footer">
          <div class="container">
            <div style="background-color:#383d61;" class="footer--bg"></div>
            <el-row>
              <el-col :span="8">
                <div class="footer_main--column">
                  <strong class="footer_main--column_title">关于我们</strong>
                  <div class="footer_about">
                    <p class="footer_about--text">
                      校园云生活平台 是全球领先的校园生活内容解决方案供应商，由前微软美国总部IE浏览器核心研发团队成员及移动互联网行业专家开发.
                    </p>
                    <p class="footer_about--text">
                      校园云生活平台也成功应用于超过100所高校，包括清华、北大、人大、北航、浙大、武大等
                    </p>
                  </div>
                </div>
              </el-col>
              <el-col :span="8">
                <div class="footer_main--column">
                  <strong class="footer_main--column_title">主要内容</strong>
                    <ul class="footer_navigation">
                      <li class="footer_navigation--item"><a href="#" class="footer_navigation--link">圈子</a></li>
                      <li class="footer_navigation--item"><a href="#" class="footer_navigation--link">促销</a></li>
                      <li class="footer_navigation--item"><a href="#" class="footer_navigation--link">学校</a></li>

                      <li class="footer_navigation--item"><a href="#" class="footer_navigation--link">活动中心</a></li>
                      <li class="footer_navigation--item"><a href="#" class="footer_navigation--link">合作加盟</a></li>
                    </ul>
                </div>
              </el-col>
              <el-col :span="8">
                <div class="footer_main--column">
                  <strong class="footer_main--column_title">联系详情</strong>
                  <ul class="footer_contact_info">
                    <li class="footer_contact_info--item"><i class="el-icon-phone"></i><span>服务专线：400 888 8888</span></li>
                    <li class="footer_contact_info--item"><i class="el-icon-message"></i><span>campus cloud life platform</span></li>
                    <li class="footer_contact_info--item"><i class="el-icon-location-information"></i><span>北京市海淀区海淀大街2号海龙大厦</span></li>
                    <li class="footer_contact_info--item"><i class="el-icon-alarm-clock"></i><span>Monday - Friday, 9am - 6 pm; </span></li>
                  </ul>
                </div>
              </el-col>
            </el-row>
          </div>
        </div>
      </el-footer>
    </el-container>
  </div>
</template>

<script>

export default {
  data () {
    return {
      form: {
        search: ''
      }
    }
  }
}
</script>
<style>
* {
  margin: 0;
  padding: 0;
  text-decoration: none;
}
/**
 * topbar
 */
 @media (min-width: 1200px){
   .container {
      width: 1170px !important;
      margin: 0 auto;
   }
 }
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}
#app .header-box {
  background-color: #7c6aa6;
  padding-top: 10px;
}
.logo {
  height: 60px;
  line-height: 30px;
  font-size: 28px;
  font-weight: 700;
  color: #fff;
}
#app .user-block {
  float: right;
}
.footer {
  width: 100%;
  background: url('assets/footer.jpg');
  background-size: cover;
  position: relative;
}
.footer .footer--bg {
  position: absolute;
  width: 100%;
  height: 100%;
  opacity: 0.95;
  top: 0;
  left: 0;
}
.footer_main--column {
  color: #fff;
  margin: 50px 0 0;
}
.footer_main--column_title {
  font-size: 17px;
  line-height: 29px;
  font-weight: 700;
  display: block;
}
.footer_about {
  position: relative;
  padding: 17px 25px 0 0;
}
.footer_about--text {
  font-size: 15px;
  line-height: 25px;
  color: #fff;
  padding: 0 0 16px;
}
.footer_navigation {
    padding: 6px 15px 0 0;
}

.footer_navigation--item {
  display: block;
  position: relative;
  padding: 12px 25px 12px 0;
  text-align: left;
  border-bottom: 1px solid rgba(255,255,255,0.1);
}
.footer_navigation--item::before{
  position: absolute;
  content: ">";
  display: block;
  right: 10px;
  top: 50%;
  transform: translate(0, -50%);
  margin-top: 3px;
  color: #fff;
  font-size: 12px;
  font-family: fontawesome;
}
.footer_navigation--link {
  color: #fff;
  font-size: 15px;
  line-height: 22px;
}
.footer_navigation--link:hover{
  text-decoration: underline;
}
.footer_contact_info {
  padding: 5px 0 0;
}
.footer_contact_info--item {
  padding: 10px 0;
  position: relative;
  color: #fff;
  font-size: 15px;
  line-height: 25px;
  list-style: none;
}
.footer_contact_info--item i{
  display: block;
  position: absolute;
  left: -2px;
  top: 12px;
}
.footer_contact_info--item span{
  display: inline-block;
  vertical-align: text-top;
  padding: 0 0 0 28px;
}
</style>
