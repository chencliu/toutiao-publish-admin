<!--  -->
<template>
  <div class="login-container">
    <div class="login_head"> 
    </div>
    <el-form ref="form" class="login-form" :model="user">
      <el-form-item>
      <el-input v-model="user.stuNum" placeholder="请输入学号"></el-input>
    </el-form-item>
    <!-- <h3>学生思想政治调研工作平台</h3> -->
    <el-form-item>
      <el-input v-model="user.mobile" placeholder="请输入手机号"></el-input>
    </el-form-item>
    <!-- <el-form-item label="验证码"> -->
    <el-form-item>
      <el-input v-model="user.code" placeholder="请输入验证码"></el-input>
    </el-form-item>
    <el-form-item>
      <el-checkbox v-model="checked">我已阅读并同意用户协议和隐私条款</el-checkbox>
    </el-form-item>
    <el-form-item >
      <el-button :plain="true" type="primary" @click="onLogin" class="login_btn">登录</el-button>
    </el-form-item>
  </el-form>
</div>
</template>

<script>
export default {
  name: 'LoginIndex',

  data () {
    return {
      user: {
          // stuNum:'',
          mobile: '',
          code: '',
        },
        checked:false  //是否同意协议的选中
    };
  },

  components: {},

  computed: {},

  mounted() {},

  methods: {
    onLogin() {
        console.log('已经点击按钮')
      }
  }
}

</script>
<style lang='less' scoped>
.login-container{
  position: fixed;
  left:0;
  right:0;
  top:0;
  bottom:0;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  background: url(./login_bg.jpg) no-repeat;
  background: cover;
  .login-form{
    background-color: #dceff1;
    padding:50px;
    min-width: 300px;
    min-height: 250px;
  }
  .login_head{
    width: 1250px;
    height: 300px;
    // margin-bottom:0px ;
    background:url("./login_logo2.png") no-repeat;
    margin-bottom:30px ;
    // text-align: center;/*主要就是这个，下面的都是样式*/
  }
  .login_btn{
    width: 100%;
  }
}
</style>