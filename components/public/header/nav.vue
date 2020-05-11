<!--
 * 头部导航组件
 * @Author: MirrorXu xupl@ilingdai.com
 -->
<style lang="scss">

</style>

<template>
  <div class="m-nav">
    <ul class="nav">
      <li class="list">
        <nuxt-link to="/my">我的美团</nuxt-link>
        <dl>
          <dd>
            <nuxt-link to="/order">我的订单</nuxt-link>
          </dd>
          <dd>
            <nuxt-link to="/order">我的搜藏</nuxt-link>
          </dd>
          <dd>
            <nuxt-link to="/order">抵用券</nuxt-link>
          </dd>
          <dd>
            <nuxt-link to="/order">账户设置</nuxt-link>
          </dd>
        </dl>
      </li>
      <li class="list">
        <nuxt-link to="/order">手机APP</nuxt-link>
      </li>
      <li class="list">
        <nuxt-link to="/center">商家中心</nuxt-link>
        <dl>
          <dd>
            <nuxt-link to="/userCenter">登录商家中心</nuxt-link>
          </dd>
          <dd>
            <nuxt-link to="/userCenter">我想合作</nuxt-link>
          </dd>
          <dd>
            <nuxt-link to="/userCenter">免费手机开店</nuxt-link>
          </dd>
          <dd>
            <nuxt-link to="/userCenter">商家申请开票</nuxt-link>
          </dd>
        </dl>
      </li>
      <li class="list">
        <nuxt-link to="/site">网站导航</nuxt-link>
        <div class="subContainer">
          <dl class="hotel">
            <dt>出行</dt>
            <dd>酒店旅游</dd>
            <dd>国际机票</dd>
            <dd>国际机票</dd>
            <dd>国际机票</dd>
            <dd>国际机票</dd>
          </dl>
          <dl class="food">
            <dt>美食</dt>
            <dd>烤鱼</dd>
            <dd>特色小吃</dd>
            <dd>外卖</dd>
          </dl>
          <dl class="movie">
            <dt>电影</dt>
            <dd>热映电影</dd>
            <dd>热映电影</dd>
            <dd>热映电影</dd>
            <dd>热映电影</dd>
          </dl>
          <dl class="app">
            <dt>手机应用</dt>
            <dd>
              <a href="">
                <img src="" alt="">
              </a>
              <a href="">
                <img src="" alt="">
              </a>
              <a href="">
                <img src="" alt="">
              </a>

            </dd>
          </dl>
        </div>
      </li>
    </ul>
  </div>
</template>

<script>
  export default {
    name: "NavBar",
    props: {},
    data() {
      return {}
    },
    computed: {},
    watch: {},
    created() {},
    mounted() {}
  }

</script>
