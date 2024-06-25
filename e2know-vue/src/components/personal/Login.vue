<template>
    <div class="outter">
        <span class="title">登录</span>
        <div class="innner">
            <el-input v-model="account" placeholder="请输入账号" class="content"></el-input>
            <el-input placeholder="请输入密码" v-model="password" show-password class="content"></el-input>
            <el-button :plain="true" @click="open2">成功</el-button>
        </div>
    </div>
</template>

<script>

export default {
  name: 'Login',
  components: {
  },
  methods:{
    open2() {
        this.$message({
          message: '登陆成功',
          type: 'success'
        });
        setTimeout(() => {
            window.location.href="/UserMainMenu"
        }, 1000);
    },
  },
  data(){
    return {
        password:"",
        account:""
    }
  }
}
</script>

<style lang="less" scoped>
.innner{
    margin: 0 32vh;
}
.title {
    font-size: 50px;
}
.el-input{
    margin: 50px 0;
}
.el-button{
    margin: 50px 50px;
}
.innner{
    border: 1px solid black;
    border-radius: 5px;
}
</style>
