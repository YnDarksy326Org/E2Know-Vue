<template>
    <div class="outter">
      <div class="card">
        <div class="head">
          <el-avatar src="https://cube.elemecdn.com/0/88/03b0d39583f48206768a7534e55bcpng.png"></el-avatar>
          YnDarksy
        </div>
        <div class="sign">
          签名：<textarea cols="30" rows="1" v-model="sign"></textarea>
        </div>
      </div>
      <div class="select">
        <div class="head">收藏</div>
        <div class="content">
          <span class="s"><img :src=imgs[0].src></span>
          <span class="s"><img :src=imgs[1].src></span>
          <span class="s"><img :src=imgs[2].src></span>
        </div>
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
  data(){
    return {
      sign:"该用户还未设置签名",
      imgs:[
      {
        src:require("E:\\E2Know\\e2know-vue\\src\\assets\\img\\4.jpg")
      },
      {
        src:require("E:\\E2Know\\e2know-vue\\src\\assets\\img\\3.jpg")
      },
      {
        src:require("E:\\E2Know\\e2know-vue\\src\\assets\\img\\1.jpg")
      }
      ]
    }
  }
}
</script>

<style lang="less" scoped>
img {
  width:100px;
  height: 50px;
}
.s {
  margin: 100px 100px;
}
.outter {
  text-align: left;
  margin: 30px 32vh;
}
.content{
  margin-left: 100px;
  margin-top: 10px;
  margin-bottom: 50px;
}
.select {
  margin-top: 50px;
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
