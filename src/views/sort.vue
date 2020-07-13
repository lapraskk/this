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
    <a-layout-content :style="{ padding: '0 50px', marginTop: '0px' }">
      <a-row :style="{ background: '#f0f2f5', padding: '70px 0px 10px 0px',width:'100%'}">
        <a-radio-group default-value="a"  :style="{float:'left',clear:'left'}">
          <a-radio-button value="a">
            综合排序
          </a-radio-button>
          <a-radio-button value="b">
            热播榜
          </a-radio-button>
          <a-radio-button value="c">
            好评榜
          </a-radio-button>
          <a-radio-button value="d">
            新上线
          </a-radio-button>
        </a-radio-group>
        <a-radio-group default-value="a"  :style="{float:'left',clear:'left'}">
          <a-radio-button value="a">
            全部地区
          </a-radio-button>
          <a-radio-button value="b">
            华语
          </a-radio-button>
          <a-radio-button value="c">
            香港地区
          </a-radio-button>
          <a-radio-button value="d">
            美国
          </a-radio-button>
          <a-radio-button value="e">
            欧洲
          </a-radio-button>
          <a-radio-button value="f">
            韩国
          </a-radio-button>
          <a-radio-button value="g">
            日本
          </a-radio-button>
          <a-radio-button value="h">
            泰国
          </a-radio-button>
          <a-radio-button value="i">
            印度
          </a-radio-button>
          <a-radio-button value="j">
            其他
          </a-radio-button>
        </a-radio-group>
        <a-radio-group default-value="a"  :style="{float:'left',clear:'left'}">
          <a-radio-button value="a">
            全部类型
          </a-radio-button>
          <a-radio-button value="b">
            喜剧
          </a-radio-button>
          <a-radio-button value="c">
            爱情
          </a-radio-button>
          <a-radio-button value="d">
            动作
          </a-radio-button>
          <a-radio-button value="e">
            枪战
          </a-radio-button>
          <a-radio-button value="f">
            犯罪
          </a-radio-button>
          <a-radio-button value="g">
            惊悚
          </a-radio-button>
          <a-radio-button value="h">
            恐怖
          </a-radio-button>
          <a-radio-button value="i">
            悬疑
          </a-radio-button>
          <a-radio-button value="j">
            动画
          </a-radio-button>
          <a-radio-button value="k">
            家庭
          </a-radio-button>
          <a-radio-button value="l">
            奇幻
          </a-radio-button>
          <a-radio-button value="m">
            魔幻
          </a-radio-button>
        </a-radio-group>
        <a-radio-group default-value="a"  :style="{float:'left',clear:'left'}">
          <a-radio-button value="a">
            全部年份
          </a-radio-button>
          <a-radio-button value="b">
            2020
          </a-radio-button>
          <a-radio-button value="c">
            2019
          </a-radio-button>
          <a-radio-button value="d">
            2018
          </a-radio-button>
          <a-radio-button value="e">
            2017
          </a-radio-button>
          <a-radio-button value="f">
            2016-2011
          </a-radio-button>
          <a-radio-button value="g">
            2010-2000
          </a-radio-button>
          <a-radio-button value="h">
            90年代
          </a-radio-button>
          <a-radio-button value="i">
            80年代
          </a-radio-button>
          <a-radio-button value="j">
            更早
          </a-radio-button>
        </a-radio-group>
      </a-row>
      <div :style="{ background: '#fff', padding: '24px', minHeight: '280px' }">
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
  name: 'sort'
}
</script>
<style scoped>
</style>
