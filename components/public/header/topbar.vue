<!--
 * @Author: MirrorXu xupl@ilingdai.com
 -->
<style lang='scss'>

</style>
<template>
  <el-row :gutter="0">
    <el-col :span="5">
      <!-- 地理位置定位  周边城市 -->
      <Geo />
    </el-col>
    <el-col :span="5">
      <User />
    </el-col>
    <el-col :span="14">
      <Navbar />
    </el-col>
  </el-row>
</template>

<script>
  import Geo from './geo'
  import User from './user'
  import Navbar from './nav'
  export default {
    name: "Topbar",
    components: {
      Geo,
      User,
      Navbar
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
