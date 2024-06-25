<template>
    <div class="outter">
      <div class="card">
        <div class="head">
          <el-avatar src="https://cube.elemecdn.com/0/88/03b0d39583f48206768a7534e55bcpng.png"></el-avatar>
          用户名
        </div>
        <div class="sign">
          签名：<span>这就是我的签名</span>
        </div>
      </div>
      <div class="select">
        <div class="head">收藏</div>
        <div class="content">收藏1</div>
      </div>
    </div>
</template>

<script>

export default {
  name: 'PersonalMainMenu',
  components: {
  },
  methods:{
  },
}
</script>

<style lang="less" scoped>
.outter {
  text-align: left;
  border: 1px solid black;
  margin: 30px 32vh;
}
.content{
  border: 1px solid black;
  margin-left: 100px;
  margin-top: 10px;
}
.select {
   border: 1px solid black;
}
.el-avatar{
  border: 1px solid black;
}
.card {
  margin: 30px 0;
  background-color: skyblue;
}
.head {
  font-size: 30px;
  margin-left: 20px;
}
.sign {
  padding-left: 50px;
  padding-top: 10px;
}
</style>
