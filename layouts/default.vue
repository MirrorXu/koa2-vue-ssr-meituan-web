<!--
 * @Author: MirrorXu xupl@ilingdai.com
-->
<template>
  <el-container class="layout-default">
    <el-header class="deafault-header">
      <MyHeader></MyHeader>
    </el-header>
    <el-main>
      <nuxt />
    </el-main>
    <el-footer>
      <div>
        <h1>footer</h1>
      </div>
    </el-footer>
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
<style lang="scss" scoped>
  @import "@/assets/css/public/layout.scss";

  .deafault-header {
    height: auto !important;
  }

</style>
