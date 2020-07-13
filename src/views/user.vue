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
      <div :style="{ background: '#f0f2f5', padding: '24px', minHeight: '800px' }">
        <a-row>
          <a-col :span="12" :style="{ background: '#fff'}">
            <a-row>
              <a-col :span="3">
                <a-avatar shape="square" :size="64" icon="user" />
              </a-col>
              <a-col :span="12" >
                <h1 margin="0px 0px 0px 0px">明日头条电影分条</h1>
                <a-textarea placeholder="Basic usage" :rows="4" />
              </a-col>
            </a-row>
          </a-col>
          <a-col :span="8" :offset="16" :style="{ background: '#fff'}">
            col-8
          </a-col>
        </a-row>
      </div>
    </a-layout-content>
    <a-layout-footer :style="{ textAlign: 'center' }">
      明日头条电影分条 ©2020 Created by FOUR
    </a-layout-footer>
  </a-layout>
</template>

<script>
export default {
  name: 'user'
}
</script>
<style>
</style>
