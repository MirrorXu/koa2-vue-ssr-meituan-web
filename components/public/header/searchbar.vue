<!--
 * @Author: MirrorXu xupl@ilingdai.com
 -->
<style lang="scss">
  @import "@/assets/css/public/header/search.scss";

</style>

<template>
  <div class="search-panel">
    <el-row class="m-header-searchbar">
      <el-col :span="3" class="left">
        <a href="/"><img src="//s0.meituan.net/bs/fe-web-meituan/e5eeaef/img/logo.png" alt="美团"></a>
      </el-col>
      <el-col :span="15" class="center">
        <div class="wrapper">
          <el-input v-model="search" placeholder="搜索商家或地点" @focus="focus" @blur="blur" @input="input" />
          <button class="el-button el-button-primary">
            <i class="el-icon-search"></i>
          </button>
          <!-- 热门搜索 -->
          <dl class="hotPlace" v-if="isHotPlace">
            <dt>热门搜索</dt>
            <dd v-for="(hotkey , i ) in hotPlace" :key="i">{{hotkey}}</dd>
          </dl>
          <!-- 搜索时推荐的关键词 -->
          <dl class="searchList" v-if="isSearchList">
            <dd v-for="(item , i) in searchList" :key="i">{{item}}</dd>
          </dl>

        </div>
        <p class="suggset">
          <a herf="#">故宫博物馆</a>
          <a herf="#">故宫博物馆</a>
          <a herf="#">故宫博物馆</a>
          <a herf="#">故宫博物馆</a>
        </p>
        <ul class="nav">
          <li>
            <nuxt-link to="/" class="takeout">美团外卖</nuxt-link>
          </li>
          <li>
            <nuxt-link to="/" class="movie">猫眼电影</nuxt-link>
          </li>
          <li>
            <nuxt-link to="/" class="hotel">美图酒店</nuxt-link>
          </li>
          <li>
            <nuxt-link to="/" class="apartment">民宿/公寓</nuxt-link>
          </li>
          <li>
            <nuxt-link to="/" class="business">商家入驻</nuxt-link>
          </li>
        </ul>
      </el-col>
      <el-col :span="6" class="right">
        <ul class="security">
          <li>
            <i class="refund"></i>
            <p class="txt">随时退</p>
          </li>
          <li>
            <i class="single"></i>
            <p class="txt">不满意免单</p>
          </li>
          <li>
            <i class="overdue"></i>
            <p class="txt">随时退</p>
          </li>
        </ul>
      </el-col>
    </el-row>
  </div>
</template>

<script>
  export default {
    name: "Searchbar",
    props: {},
    data() {
      return {
        // 输入框是否聚焦
        isFocus: false,
        // 搜索框中用户输入的值
        search: '',
        hotPlace: ['热搜词1', '热搜词2', '热搜词3'],
        searchList: ['推荐词1', '推荐词2', '推荐词3', '推荐词4', ]
      }
    },
    computed: {
      isHotPlace() {
        return this.isFocus && !this.search
      },
      isSearchList() {
        return this.isFocus && this.search
      }
    },
    methods: {
      focus() {
        this.isFocus = true
      },
      blur() {
        const timer = setTimeout(() => {
          this.isFocus = false;
          clearTimeout(timer)
        }, 200)
      },
      input(e) {
        console.log('input:', e);

      }
    },
    watch: {},
    created() {},
    mounted() {}
  }

</script>
