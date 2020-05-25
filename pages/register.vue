<style lang="scss" scoped>
  @import "@/assets/css/register/index.scss";

</style>

<template>
  <div class="page-register">
    <!-- 头部 -->
    <article class="header">
      <header>
        <a href="/" class="site-logo"></a>
        <span class="login">
          <em class="bold">已有美团账号？</em>
          <a href="login">
            <el-button type="primary" size="small">登录</el-button>
          </a>
        </span>
      </header>
    </article>
    <!-- 内容 -->
    <section>

      <el-form :ref="ruleForm" :rules="rules" :model="ruleForm" label-width="100px" class="demo-ryleForm"
        label-position="right">

        <el-form-item label="昵称" prop="name">
          <el-input v-model="ruleForm.name" />
        </el-form-item>

        <el-form-item label="邮箱" prop="email">
          <el-input v-model="ruleForm.email"></el-input>
          <el-button size="mini" round @click="sendMsg">发送验证码</el-button>
          <span class="status">{{statusMsg}}</span>
        </el-form-item>

        <el-form-item label="验证码" prop="code">
          <el-input v-model="ruleForm.code" maxlength="4"></el-input>
        </el-form-item>

        <el-form-item label="密码" prop="pwd">
          <el-input v-model="ruleForm.pwd" type="password"></el-input>
        </el-form-item>

        <el-form-item label="确认密码" prop="cpwd">
          <el-input v-model="ruleForm.cpwd" type="password"></el-input>
        </el-form-item>

        <el-form-item>
          <el-button type="primary" size="mini" @click="register">同意并注册</el-button>
        </el-form-item>

      </el-form>
    </section>
  </div>
</template>

<script>
  export default {
    name: "",
    layout: 'blank',
    props: {},
    data() {
      return {
        statusMsg: "",
        ruleForm: {
          name: '',
          email: '',
          code: '',
          pwd: '',
          cpwd: ''
        },
        // 表单校验规则
        rules: {
          name: [{
            required: true,
            type: 'string',
            message: '请输入昵称',
            trigger: 'blur'
          }],
          email: [{
            required: true,
            type: 'email',
            message: '邮箱地址不合法',
            trigger: 'blur'
          }],
          pwd: [{
            required: true,
            message: '密码输入不合法',
            trigger: 'blur'
          }],
          cpwd: [{
            required: true,
            message: '密码输入不合法',
            trigger: 'blur'
          }, {
            validator: (rule, value, callback) => {
              // debugger
              if (value === '') {
                callback(new Error('请再次输入密码'))
              } else if (value !== this.ruleForm.pwd) {
                callback(new Error('两次输入的密码不一致'))
              } else {
                callback()
              }
            },
            trigger: 'blur'
          }]
        }
      }
    },
    methods: {
      sendMsg() {
        alert('发送验证码')
      },
      register() {
        alert('注册')
      },
      onSubmit() {
        alert('submit!');
      }
    }
  }

</script>
