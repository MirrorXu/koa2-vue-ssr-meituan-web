<!--
 * @Author: MirrorXu xupl@ilingdai.com
 -->
<style lang="scss">
  @import "@/assets/css/public/header.scss";

</style>

<template>
  <div class="m-header">
    <el-row>
      <el-col>
        <Topbar></Topbar>
      </el-col>
    </el-row>
    <el-row>
      <el-col>
        <Searchbar />
      </el-col>
    </el-row>
  </div>
</template>

<script>
  import Topbar from './topbar'
  import Searchbar from './searchbar'
  export default {
    name: "MyHeader",
    components: {
      Topbar,
      Searchbar
    },
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
