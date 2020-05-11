<!--
 * @Author: MirrorXu xupl@ilingdai.com
 -->
<style lang="scss" scoped>

</style>

<template>
  <div class="wrap">
    <div class="m-user">
      <!-- 登录状态 -->
      <template v-if="user">
        欢迎您！<span class="username">{{user}}</span>
        <nuxt-link to="/exit">退出</nuxt-link>
      </template>
      <!-- 未登录状态 -->
      <template v-else>
        <nuxt-link to="/login" class="login">立刻登录</nuxt-link>
        <nuxt-link to="/register" class="register">注册</nuxt-link>
      </template>
    </div>
  </div>
</template>

<script>
  export default {
    name: "User",
    props: {},
    data() {
      return {
        user: ''
      }
    },
    computed: {},
    watch: {},
    created() {},
    mounted() {}
  }

</script>
