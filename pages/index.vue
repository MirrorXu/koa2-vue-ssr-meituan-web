<template>
  <div class="page-index">
    <h1>index页面</h1>
    <el-row>
      <el-col :span="5">
        <Emenu></Emenu>
      </el-col>
      <el-col :span="19">2</el-col>
    </el-row>
    <el-row :span="24">3</el-row>
  </div>
</template>

<script>
  import Emenu from '@/components/index/menu.vue'
  export default {
    components: {
      Emenu
    },
    data() {
      return {
        title: 'Mirror title'
      }
    }
  }

</script>

<style lang="scss">
  @import "@/assets/css/index/index.scss";

  .page-index {
    display: block;
    width: 100%;
    margin-top: 30px;
    background-color: sandybrown;
  }

</style>
