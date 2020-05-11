<!--
 * 地理位置定位  周边城市
 * @Author: MirrorXu xupl@ilingdai.com
 *
 -->

<style scoped>

</style>

<template>
  <div class="wrap">
    <i class="el-icon-location" /> 北京市
    <nuxt-link class="changeCity" to="changeCity">切换城市</nuxt-link>
    [香河 廊坊 天津]
  </div>
</template>

<script>
  export default {
    name: "Geo",
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
