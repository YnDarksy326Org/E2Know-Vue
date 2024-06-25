<template>
    <div class="outter">
        <el-card :body-style="{ padding: '0px' }">
            <div class="name">Nuraphone NuraTrue Pro</div>
            <img src="../../assets/img/earpic.jpg" class="image" shadow="always">
        </el-card>
        <div class="data">Nuraphone NuraTrue Pro 规格与价格</div>
        <div>
            <div class="Title"><span>规格参数</span></div>
            <div class="cardoutter">
                <div class="box-card" style="hover">
                <div slot="header" class="clearfix">
                    <i class="el-icon-headset"></i>
                    <span>音质</span>
                </div>
                <div v-for="o in 1" :key="o" class="text item">
                    {{'最高频率：' + "40000 Hz" }}
                </div>
                </div>
                <div class="box-card">
                <div slot="header" class="clearfix">
                    <i class="el-icon-paperclip"></i>
                    <span>连接方式</span>
                </div>
                <div v-for="o in 1" :key="o" class="text item">
                    {{'无线连接方式：' + "蓝牙" }}
                    <div></div>
                    {{'有线连接方式：' + "typec" }}
                </div>
                </div>
                <div class="box-card">
                <div slot="header" class="clearfix">
                    <i class="el-icon-view"></i>
                    <span>降噪</span>
                </div>
                <div v-for="o in 1" :key="o" class="text item">
                    {{'降噪强度：' + "30db" }}
                </div>
                </div>
            </div>
        </div>
        <div>
            <div class="Title"><span>用户评论</span></div>
            <div class="conments">
                <div class="inner">
                    <div v-for="(o,index) in commentsData" :key="index">
                        <img class="pic" :src="o.picurl">
                        <div class="username">{{o.username}}</div>
                        <div class="contenttext">{{o.comments}}</div>
                    </div>
                </div>
                <el-input 
                :autosize="{ minRows: 4, maxRows: 20}" 
                type="textarea"
                placeholder="请输入你的评论"
                v-model="textarea">
                </el-input>
                <el-button type="primary" @click="commit">发表评论</el-button>
            </div>
        </div>
    </div>
</template>

<script>

export default {
  name: 'MainContent',
  components: {
  },
  data(){
    return {
        textarea:"",
        commentsData:[
            {
                username:"YnDarksy",
                comments:"哈哈哈，这个耳机太坑了",
                picurl:require("E:\\E2Know\\e2know-vue\\src\\assets\\img\\earpic.jpg")
            },
            {
                username:"杨定鑫",
                comments:"耳机音质非常好",
                picurl:require("E:\\E2Know\\e2know-vue\\src\\assets\\img\\earpic.jpg")
            }
        ]
    }
  },
  methods:{
    commit(){
        this.commentsData.push({
            username:"杨定鑫",
            comments:this.textarea,
            picurl:require("E:\\E2Know\\e2know-vue\\src\\assets\\img\\earpic.jpg")
        })
        this.textarea = ""
    }
  },

}
</script>

<style lang="less" scoped>
.cardoutter {
    text-align: left;
    margin: 0 35vh;
}
.item {
    margin: 40px 20px;
    font: 20px;
}
.clearfix {
    margin: 10px 10px;
    font-size: 30px;
}
.box-card {
    display: inline-block;
    margin-right: 230px;
    border: solid 1px black;
    width: 300px;
    box-shadow: 0 0 5px 1px #999 ;
    border-radius: 5px;
}
.contenttext {
    margin-left: 90px;
    margin-top: 10px;
    margin-bottom: 10px;
}
.pic {
    height: 50px;
    width: 50px;
    display: inline-block;
    text-align: left;
}
.username {
    font-size: 20px;
    text-align: left;
    padding: 10px 20px;
    display: inline-block;
}
.el-button {
    margin-top: 10px;
    margin-bottom: 10px;
}
.inner {
    margin-bottom: 30px;
    margin-top: 30px;
    text-align: left;
}
.conments {
    margin: 10px 35vh;
    word-break: break-all;
    word-wrap: break-word;
    white-space: pre-wrap;
}
.Title {
    font-size: 40px;
    font-weight: bolder;
    text-align: left;
    margin-left: 32vh;
    padding: 30px 0;
}
.outter {
    height: 100vh;
}
span {
    border-bottom: solid #28292a 1px;
    padding-bottom: 5px;
}
.data {
    font-size: 40px;
    padding: 10px 10px;
}
.name {
    font-size: 30px;
    padding: 20px 20px;
}
.el-card {
    text-align: center;
    background-color: white;
    margin-left: 32vh;
    margin-right: 32vh;
    margin-top: 50px;
    border-bottom: 1px solid #999;
}
img {
    height: 300px;
    width: 300px;
    margin: 10px 10px;
}
</style>
