<template>
    <div>
        <div class="down">
            <div class="content2">耳机参数展示</div>
        </div>
        <el-container>
            <div class="outter">
                <div class="search">
                    <div class="SortText">排序方式</div>
                    <el-select v-model="value" placeholder="请选择">
                        <el-option
                        v-for="item in options"
                        :key="item.value"
                        :label="item.label"
                        :value="item.value">
                        </el-option>
                    </el-select>
                </div>
            </div>
            <div class="content">
                <el-row :gutter="10" >
                <el-col  :span="12" v-for="(o, index) in cards" :key="index" >
                    <el-card :body-style="{ padding: '5px' }">
                            <img :src="o.imgurl" class="image" shadow="always" @click="showEarPhone">
                            <div class="itemname">{{o.name}}</div>
                            <div>
                                <span class="item">续航:10h</span>
                                <span class="item">重量:10h</span>
                            </div>
                            <div>
                                <span class="item">防水:10h</span>
                                <span class="item">麦克风数:10h</span>
                            </div>
                    </el-card>
                </el-col>
                </el-row>
            </div>
        </el-container>
    </div>
</template>

<script>
export default {
  name: 'UserMainMenu',
  components: {

  },
  methods:{
    showEarPhone(){
        this.$router.push('/earMainMenu');
        console.log("点击了图片")
    }
  },
  data() {
      return {
        cards:[
            {
                ID:"1",
                imgurl:"../../assets/img/earpic.jpg",
                name:"耳机2",
                battylife:"",
                weight:"",
                Protection_IP_rating:"",
                microphone_number:""
            },
            {
                ID:"1",
                imgurl:"../../assets/img/earpic.png",
                name:"耳机2",
                battylife:"",
                weight:"",
                Protection_IP_rating:"",
                microphone_number:""
            },
            {
                ID:"1",
                imgurl:"../../assets/img/earpic.png",
                name:"耳机2",
                battylife:"",
                weight:"",
                Protection_IP_rating:"",
                microphone_number:""
            },
            {
                ID:"1",
                imgurl:"../../assets/img/earpic.png",
                name:"耳机2",
                battylife:"",
                weight:"",
                Protection_IP_rating:"",
                microphone_number:""
            },
            {
                ID:"1",
                imgurl:"../../assets/img/earpic.png",
                name:"耳机2",
                battylife:"",
                weight:"",
                Protection_IP_rating:"",
                microphone_number:""
            },
            {
                ID:"1",
                imgurl:"../../assets/img/earpic.png",
                name:"耳机2",
                battylife:"",
                weight:"",
                Protection_IP_rating:"",
                microphone_number:""
            },
            {
                ID:"1",
                imgurl:"../../assets/img/earpic.png",
                name:"耳机2",
                battylife:"",
                weight:"",
                Protection_IP_rating:"",
                microphone_number:""
            },
            {
                ID:"1",
                imgurl:"../../assets/img/earpic.png",
                name:"耳机2",
                battylife:"",
                weight:"",
                Protection_IP_rating:"",
                microphone_number:""
            },
            {
                ID:"1",
                imgurl:"../../assets/img/earpic.png",
                name:"耳机2",
                battylife:"",
                weight:"",
                Protection_IP_rating:"",
                microphone_number:""
            },
            {
                ID:"1",
                imgurl:"../../assets/img/earpic.png",
                name:"耳机2",
                battylife:"",
                weight:"",
                Protection_IP_rating:"",
                microphone_number:""
            },
            {
                ID:"1",
                imgurl:"../../assets/img/earpic.png",
                name:"耳机2",
                battylife:"",
                weight:"",
                Protection_IP_rating:"",
                microphone_number:""
            },
            {
                ID:"1",
                imgurl:"../../assets/img/earpic.png",
                name:"耳机2",
                battylife:"",
                weight:"",
                Protection_IP_rating:"",
                microphone_number:""
            },
            {
                ID:"1",
                imgurl:"../../assets/img/earpic.png",
                name:"耳机2",
                battylife:"",
                weight:"",
                Protection_IP_rating:"",
                microphone_number:""
            },
            {
                ID:"1",
                imgurl:"../../assets/img/earpic.png",
                name:"耳机2",
                battylife:"",
                weight:"",
                Protection_IP_rating:"",
                microphone_number:""
            },
            {
                ID:"1",
                imgurl:"../../assets/img/earpic.png",
                name:"耳机3",
                battylife:"",
                weight:"",
                Protection_IP_rating:"",
                microphone_number:""
            },
            {
                ID:"1",
                imgurl:"../../assets/img/earpic.png",
                name:"耳机4",
                battylife:"",
                weight:"",
                Protection_IP_rating:"",
                microphone_number:""
            },
            {
                ID:"1",
                imgurl:"../../assets/img/earpic.png",
                name:"耳机5",
                battylife:"",
                weight:"",
                Protection_IP_rating:"",
                microphone_number:""
            },
            {
                ID:"1",
                imgurl:"../../assets/img/earpic.png",
                name:"耳机6",
                battylife:"",
                weight:"",
                Protection_IP_rating:"",
                microphone_number:""
            },
            {
                ID:"1",
                imgurl:"../../assets/img/earpic.png",
                name:"耳机7",
                battylife:"",
                weight:"",
                Protection_IP_rating:"",
                microphone_number:""
            },
            {
                ID:"1",
                imgurl:"../../assets/img/earpic.png",
                name:"耳机8",
                battylife:"",
                weight:"",
                Protection_IP_rating:"",
                microphone_number:""
            },
            {
                ID:"1",
                imgurl:"../../assets/img/earpic.png",
                name:"耳机9",
                battylife:"",
                weight:"",
                Protection_IP_rating:"",
                microphone_number:""
            },
            {
                ID:"1",
                imgurl:"../../assets/img/earpic.png",
                name:"耳机9",
                battylife:"",
                weight:"",
                Protection_IP_rating:"",
                microphone_number:""
            },
            {
                ID:"1",
                imgurl:"../../assets/img/earpic.png",
                name:"耳机9",
                battylife:"",
                weight:"",
                Protection_IP_rating:"",
                microphone_number:""
            },
            {
                ID:"1",
                imgurl:"../../assets/img/earpic.png",
                name:"耳机9",
                battylife:"",
                weight:"",
                Protection_IP_rating:"",
                microphone_number:""
            },
            {
                ID:"1",
                imgurl:"../../assets/img/earpic.png",
                name:"耳机9",
                battylife:"",
                weight:"",
                Protection_IP_rating:"",
                microphone_number:""
            },
            {
                ID:"1",
                imgurl:"../../assets/img/earpic.png",
                name:"耳机9",
                battylife:"",
                weight:"",
                Protection_IP_rating:"",
                microphone_number:""
            },
            {
                ID:"1",
                imgurl:"../../assets/img/earpic.png",
                name:"耳机9",
                battylife:"",
                weight:"",
                Protection_IP_rating:"",
                microphone_number:""
            },
            {
                ID:"1",
                imgurl:"../../assets/img/earpic.png",
                name:"耳机9",
                battylife:"",
                weight:"",
                Protection_IP_rating:"",
                microphone_number:""
            },
            {
                ID:"1",
                imgurl:"../../assets/img/earpic.png",
                name:"耳机9",
                battylife:"",
                weight:"",
                Protection_IP_rating:"",
                microphone_number:""
            },
            {
                ID:"1",
                imgurl:"../../assets/img/earpic.png",
                name:"耳机9",
                battylife:"",
                weight:"",
                Protection_IP_rating:"",
                microphone_number:""
            },
        ],
        options: [{
          value: '1',
          label: '价格升序'
        }, {
          value: '2',
          label: '价格降序'
        }, {
          value: '3',
          label: '评分升序'
        }, {
          value: '4',
          label: '评分降序'
        },],
        value: ''
      }
    }
}
</script>

<style lang="less" scoped>
.itemname {
    margin-bottom: 10px;
    font-size: 30px;
}
.item {
    margin: 10px 10px;
    text-align: left;
}
.content2 {
    padding-left: 32vh;
}
.down {
    height: 135px;
    background: -webkit-linear-gradient(left,rgb(15, 1, 56), rgb(160, 160, 241));
    font-size: 30px;
    color: white;
    text-align: left;
    line-height: 100px;
}
.el-card {
    border: solid 1px gray;
    margin-bottom: 70px;
    cursor: pointer;
    border-radius: 5px;
    width: 600px;
    box-shadow: 0 0 5px 1px #999 ;
}
.el-select {
    margin: 10px 10px;
}
.SortText {
    text-align: left;
    padding: 10px 10px;
    font-weight: bolder;
}
img {
    width: 200px;
    height: 100px;
}
.content {
    margin-top: 10px;
    margin-left: 100px;
    margin-right: 32vh;
}
.el-select {
    padding-bottom: 10px;
}
.search {
    box-shadow: 0 0 5px 1px #999 ;
    border: solid 1px #999;
    border-radius: 10px;
    top: 10px;
    position: sticky;
    width: 200px;
}
.outter {
    float:left;
    top:2px;
    margin-left:32vh;
    margin-right:10px;
    margin-top:10px;
    //border: solid 1px #999;
    background-color: white;
}
</style>
