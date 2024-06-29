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
                        @click.native="sortearphone"
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
                            <div class="datae">
                                <span class="item">续航:{{o.battylife}}</span>
                                <span class="item">重量:{{o.weight}}</span>
                            </div>
                            <div class="datae">
                                <span class="item">防水:{{o.Protection_IP_rating}}</span>
                                <span class="item">麦克风数:{{o.microphone_number}}</span>
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
    },
    sortearphone(){
        console.log(this.value)
        if(this.value==1){
            this.cards.sort((a,b)=>{
                return a.price-b.price
            })
        }
        else{
            this.cards.sort((a,b)=>{
                return b.price-a.price
            })
        }

    }
  },
  data() {
      return {
        value:"",
        cards:[
            {
                ID:"1",
                imgurl:require("../../assets/img/earpic.jpg"),
                name:"Nuraphone NuraTrue Pro",
                battylife:"8h",
                weight:"17.2g",
                price:100,
                Protection_IP_rating:"ipx4",
                microphone_number:"8"
            },
            {
                ID:"2",
                imgurl:require("../../assets/img/1.jpg"),
                name:"Bowers & Wilkins Pi7 S2",
                battylife:"5h",
                weight:"14g",
                price:200,
                Protection_IP_rating:"ip54",
                microphone_number:"6",
            },
            {
                ID:"3",
                imgurl:require("../../assets/img/2.jpg"),
                name:"Cambridge Audio Melomania M100",
                battylife:"16h",
                weight:"13.3g",
                price:1323,
                Protection_IP_rating:"ipx4",
                microphone_number:"6",
            },
            {
                ID:"4",
                imgurl:require("../../assets/img/3.jpg"),
                name:"Denon PerL Pro",
                battylife:"32h",
                weight:"13.3g",
                Protection_IP_rating:"ipx4",
                microphone_number:"8",
                price:300,
            },
            {
                ID:"5",
                imgurl:require("../../assets/img/4.jpg"),
                name:"LG Tone Free T90",
                battylife:"9h",
                weight:"11.1g",
                Protection_IP_rating:"ipx4",
                microphone_number:"6",
                price:1029,
            },
            {
                ID:"6",
                imgurl:require("../../assets/img/5.jpg"),
                name:"OnePlus Buds Pro 2",
                battylife:"9h",
                weight:"9.8g",
                Protection_IP_rating:"ip55",
                microphone_number:"6",
                price:124,
            },
            {
                ID:"7",
                imgurl:require("../../assets/img/6.jpg"),
                name:"Realme Buds Air 5 Pro",
                battylife:"11h",
                weight:"10g",
                Protection_IP_rating:"ipx5",
                microphone_number:"6",
                price:2019,
            },
            {
                ID:"8",
                imgurl:require("../../assets/img/7.jpg"),
                name:"Sennheiser Momentum True Wireless 3",
                battylife:"7h",
                weight:"10.6g",
                Protection_IP_rating:"ipx4",
                microphone_number:"6",
                price:1234,
            },
            {
                ID:"9",
                imgurl:require("../../assets/img/8.jpg"),
                name:"Sennheiser Momentum True Wireless 3",
                battylife:"7h",
                weight:"10.6g",
                Protection_IP_rating:"ipx4",
                microphone_number:"6",
                price:1231,
            },
        ],
        options: [{
          value: '1',
          label: '价格升序'
        }, {
          value: '2',
          label: '价格降序'
        },],
        value: ''
      }
    },
}
</script>

<style lang="less" scoped>
.itemname {
    margin: 20px 0;
    font-size: 30px;
}
.datae{
    margin: 20px 20px;
}
.item {
    text-align: left;
    margin: 20px 20px;
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
    margin-bottom: 70px;
    cursor: pointer;
    border-radius: 5px;
    width: 600px;
    box-shadow: 0 0 5px 1px #999 ;
    border-bottom: 1px solid #999;
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
    width: 100px;
    height: 70px;
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
