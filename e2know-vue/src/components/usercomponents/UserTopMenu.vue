<template>
    <div class="outter">
        <div class="upper">
            <div class="leftcontent">
                <span class="content" @click="backtomain">易知耳</span>
                <i class="el-icon-search" style="color:white"></i>
                <input type="text" v-model="input" placeholder="   请输入查找耳机名">
            </div>
            <div class="rightcontent">
            <el-dropdown>
                <span class="el-dropdown-link">
                <i class="el-icon-user-solid"></i><i class="el-icon-arrow-down el-icon--right"></i>
                </span>
                <el-dropdown-menu slot="dropdown">
                <el-dropdown-item @click.native="personalData">个人资料</el-dropdown-item>
                <el-dropdown-item @click.native="login">登录</el-dropdown-item>
                </el-dropdown-menu>
            </el-dropdown>
            </div>
        </div>
    </div>
</template>
<script>
  export default {
    name:"UserTopMenu",
    data() {
      return {
        activeIndex: '1',
        activeIndex2: '1',
        username:"杨定鑫",
        input:""
      };
    },
    methods: {
      backtomain() {
        this.$router.push('/UserMainMenu');
      },
      personalData(){
        window.location.href="/PersonalMainMenu"
      },
      login(){
        window.location.href="/Login"
      }
    }
  }
</script>
<style scoped>
body,html{
  padding: 0;
  margin: 0;
}
.upper {
    height: 60px;
    background-color: black;
    clear: both;
}
.content {
    width: 200px;
    font-size: 50px;
    float: left;
    color:white;
    cursor: pointer;
}

input {
    height: 30px;
    border: white;
    margin-left: 10px;
    border-radius: 2px;
}
.leftcontent {
    height: 60px;
    float: left;
    padding-left: 30vh
}
.rightcontent {
  float: right;
  padding-right: 60px;
}
.el-dropdown-link {
  cursor: pointer;
  color: #fff;
}
.el-icon-arrow-down {
  font-size: 12px;
}
.el-button{
  background-color: #545c64;
  border: #545c64;
}
</style>