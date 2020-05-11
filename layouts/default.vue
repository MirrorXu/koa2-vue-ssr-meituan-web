<template>
  <el-container class="layout-default">
    <el-header>
      <MyHeader></MyHeader>
    </el-header>
    <el-main>
      <nuxt />
    </el-main>
    <el-footer>Footer</el-footer>
  </el-container>
</template>

<script>
  import MyHeader from '@/components/public/header/index'
  export default {
    name: "DefaultLayout",
    components: {
      MyHeader
    }
  }

</script>
<style lang="scss">
  @import "@/assets/css/public/layout.scss";

</style>
