<template>
  <el-container>
      <!-- 顶栏 -->
      <el-header height="60px">
        <UserTopMenu></UserTopMenu>
      </el-header>
      <el-main>
        <router-view></router-view>
      </el-main>
  </el-container>
</template>

<script>
import UserTopMenu from '../components/usercomponents/UserTopMenu.vue'
import UserMainMenu from '../components/usercomponents/UserMainMenu.vue'

export default {
  name: 'mainMenu',
  components: {
    UserTopMenu,
    UserMainMenu
  },
  data() {
    return {
      route:this.$route.path
    }
  },
}
</script>

<style lang="less" scoped>
.el-header, .el-footer {
    height: 260px;
    text-align: center;
    line-height: 60px;
    padding: 0;
    margin: 0;
  }

  
  .el-main {
    /* background-color: #E9EEF3;
    color: #333; */
    text-align: center;
    padding: 0;
    margin: 0;
    height: 100vh;
  }
  
  body > .el-container {
    margin-bottom: 40px;
  }
  .el-container {
    height: 100vh;
  }
  .el-container:nth-child(5) .el-aside,
  .el-container:nth-child(6) .el-aside {
    line-height: 260px;
  }
  
  .el-container:nth-child(7) .el-aside {
    line-height: 320px;
  }
</style>
