<template>
  <a-layout id="components-layout-demo-fixed">
    <a-layout-header :style="{ position: 'fixed', zIndex: 1, width: '100%' }">
      <a-row>
        <a-col :span="3">
          <img src="../assets/logo.png"
               :style="{ width:'auto',height:'50px',margin:' 4px  0px 0px 0px',float: left}">
        </a-col>
        <a-col :span="6">
          <a-input-search
            placeholder="搜索你想看的电影"
            size="large"
            :style="{width:'400px',marginLeft:'20px',marginTop: '11px',position: 'fixed'}"
            @search="onSearch" />
        </a-col>
        <a-col :span="8" :offset="12">
          <a-menu v-model="current" mode="horizontal" theme="dark" :style="{ lineHeight: '60px' }">
            <a-menu-item key="1">
              <router-link to="/">首页</router-link>
            </a-menu-item>
            <a-menu-item key="2">
              <router-link to="/recommend">电影推荐</router-link>
            </a-menu-item>
            <a-menu-item key="3">
              <router-link to="/sort">电影分类</router-link>
            </a-menu-item>
            <a-menu-item key="4">
              <router-link to="/about">登录</router-link>
            </a-menu-item>
            <a-menu-item key="5">
              <router-link to="/user">个人中心</router-link>
            </a-menu-item>
          </a-menu>
        </a-col>
      </a-row>
    </a-layout-header>
    <a-layout-content :style="{ padding: '0 50px', marginTop: '90px' }">
      <a-row :style="{ background: '#f0f2f5', padding: '0px 0px 30px 0px',width:'100%'}">
        <a-carousel arrows autoplay>
          <div
            slot="prevArrow"
            class="custom-slick-arrow"
            style="left: 10px;zIndex: 1"
          >
            <a-icon type="left-circle" />
          </div>
          <div slot="nextArrow" class="custom-slick-arrow" style="right: 10px">
            <a-icon type="right-circle" />
          </div>
          <div><img src="../assets/1.jpg"
                    :style="{ width:'auto',height:'700px',align:'center'}"></div>
          <div><h3>2</h3></div>
          <div><h3>3</h3></div>
          <div><h3>4</h3></div>
        </a-carousel>
      </a-row>
      <div :style="{ background: '#fff', padding: '24px', minHeight: '800px' }">
        Content
      </div>
    </a-layout-content>
    <a-layout-footer :style="{ textAlign: 'center' }">
      明日头条电影分条 ©2020 Created by FOUR
    </a-layout-footer>
  </a-layout>
</template>
<script>
export default {
  name: 'menu'
}
</script>
<style scoped>
  /* For demo */
  .ant-carousel >>> .slick-slide {
    text-align: center;
    height: 550px;
    line-height: 160px;
    background: #364d79;
    overflow: hidden;
  }

  .ant-carousel >>> .custom-slick-arrow {
    width: 25px;
    height: 25px;
    font-size: 25px;
    color: #fff;
    background-color: rgba(31, 45, 61, 0.11);
    opacity: 0.3;
  }
  .ant-carousel >>> .custom-slick-arrow:before {
    display: none;
  }
  .ant-carousel >>> .custom-slick-arrow:hover {
    opacity: 0.5;
  }

  .ant-carousel >>> .slick-slide h3 {
    color: #fff;
  }
</style>
