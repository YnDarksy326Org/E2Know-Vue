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
        <div class="head">收藏：</div>
        <div class="content">
          <el-table
            :data="tableData"
            style="width: 100%">
            <el-table-column
              prop="date"
              label="日期"
              width="300">
            </el-table-column>
            <el-table-column
              prop="name"
              label="型号"
              width="300">
            </el-table-column>
            <el-table-column
              prop="address"
              label="价格">
            </el-table-column>
            <el-table-column>
              <el-button
                size="mini"
                type="normal`"
                @click="handleDelete(scope.$index, scope.row)">查看
              </el-button>
              <el-button
                size="mini"
                type="danger"
                @click="handleDelete(scope.$index, scope.row)">删除
              </el-button>
            </el-table-column>
          </el-table>
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
      ],
      tableData: [{
        date: '2024-05-02',
        name: 'wf-xm5',
        address: '1000￥'
      }, {
        date: '2024-05-04',
        name: 'freebuts pro',
        address: '700￥'
      }, {
        date: '2024-05-01',
        name: 'Nuraphone NuraTrue Pro',
        address: '200￥'
      }, {
        date: '2024-05-03',
        name: 'Bowers & Wilkins Pi7 S2',
        address: '300￥'
      }]
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
  border-radius: 5px;
}
.el-avatar{
  border: 1px solid black;
}
.card {
  padding-bottom: 30px;
  padding-top: 5px;
  background-color: skyblue;
  border-radius: 5px;
}
.head {
  font-size: 30px;
  margin-left: 20px;
  margin-top: 30px;
}
.sign {
  padding-left: 50px;
  padding-top: 10px;
}
</style>
