<template>
    <el-container>
        <MainContent></MainContent>
    </el-container>
</template>

<script>
import UserTopMenu from '../usercomponents/UserTopMenu.vue'
import MainContent from './MainContent.vue'

export default {
  name: 'earMainMenu',
  components: {
    UserTopMenu,
    MainContent
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
