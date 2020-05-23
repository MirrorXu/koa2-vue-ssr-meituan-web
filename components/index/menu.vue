<style lang="scss" scoped>

</style>

<template>
  <div class="m-menu" @mouseleave="mouseleave">
    <dl class="nav">
      <dt>全部分类</dt>
      <dd v-for="(item , index) in menu" :key="index" @mouseenter="enter(item)">
        <i :class="item.type" />
        {{item.name}}
        <span class="arrow" />
      </dd>
    </dl>
    <div class="detail" v-show="kind">
      <template v-for="(item ,index) in curDetail">
        <h4 :key="index">{{item.title}}</h4>
        <template v-if="item.child">
          <span v-for="(tag , i) in item.child" :key="tag">{{tag}}</span>
        </template>
      </template>
    </div>
  </div>
</template>

<script>
  export default {
    name: "menu",
    props: {},
    data() {
      return {
        kind: '',
        menu: [{
          name: '美食',
          type: 'food',
          children: [{
            title: '美食',
            child: ['代金券', '甜点', '饮料', '火锅']
          }]
        }, {
          type: 'takeout',
          name: '外卖',
          children: [{
            title: '外卖',
            child: ['代金券', '甜点', '饮料', '火锅']
          }]
        }, {
          type: 'hotel',
          name: '酒店',
          children: [{
            title: '酒店',
            child: ['代金券', '甜点', '饮料', '火锅']
          }]
        }]
      }
    },
    computed: {
      curDetail() {
        const kind = this.kind
        if (this.kind) {
          return this.menu.filter(item => item.name === kind)[0].children
        } else {
          return null
        }
      }
    },
    methods: {
      mouseleave() {
        let timer = setTimeout(() => {
          this.kind = ''
          timer = null
        }, 150)
      },
      enter(item) {
        console.log(item.name);
        this.kind = item.name
      }
    },
    watch: {},
    created() {},
    mounted() {}
  }

</script>
