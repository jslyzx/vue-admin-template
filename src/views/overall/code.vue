<template>
  <div class="app-container switchBg">
    <div class="h-title">分类编码库</div>
    <div class="search switchBg">
      <el-row>
        <el-col :span="6">
          <el-input placeholder="请输入内容" v-model="keyword" style="padding: 24px;">
            <el-button slot="append">搜索</el-button>
          </el-input>
        </el-col>
      </el-row>
    </div>
    <div class="list">
      <div class="item switchBg">
        <img src="@/assets/code/pic-1.png" />
        <div class="name switchText">船舶能耗数据收集管理办法</div>
        <div class="date switchText">更新时间：2022-03-31</div>
        <el-row class="bottom">
          <div @click="download('http://117.144.170.42:8089/prod-api/profile/pdfs/船舶能耗数据收集管理办法.pdf')">
            <el-col :span="12" class="switchText">
              <i class="el-icon-download"></i>下载
            </el-col>
          </div>
          <div @click="download('http://117.144.170.42:8089/prod-api/profile/pdfs/船舶能耗数据收集管理办法.pdf')">
            <el-col :span="12" class="switchText">
              <i class="el-icon-view"></i>查看
            </el-col>
          </div>
        </el-row>
      </div>
      <div class="item switchBg">
        <img src="@/assets/code/pic-2.png" />
        <div class="name switchText">船舶总装建造智能化标准体系建设指南</div>
        <div class="date switchText">更新时间：2022-03-31</div>
        <el-row class="bottom">
          <div @click="download('http://117.144.170.42:8089/prod-api/profile/pdfs/船舶总装建造智能化标准体系建设指南.pdf')">
            <el-col :span="12" class="switchText">
              <i class="el-icon-download"></i>下载
            </el-col>
          </div>
          <div @click="download('http://117.144.170.42:8089/prod-api/profile/pdfs/船舶总装建造智能化标准体系建设指南.pdf')">
            <el-col :span="12" class="switchText">
              <i class="el-icon-view"></i>查看
            </el-col>
          </div>
        </el-row>
      </div>
      <div class="item switchBg">
        <img src="@/assets/code/pic-3.png" />
        <div class="name switchText">工业互联网标识行业应用指南（船舶）</div>
        <div class="date switchText">更新时间：2022-03-31</div>
        <el-row class="bottom">
          <div @click="download('http://117.144.170.42:8089/prod-api/profile/pdfs/工业互联网标识行业应用指南（船舶）.pdf')">
            <el-col :span="12" class="switchText">
              <i class="el-icon-download"></i>下载
            </el-col>
          </div>
          <div @click="download('http://117.144.170.42:8089/prod-api/profile/pdfs/工业互联网标识行业应用指南（船舶）.pdf')">
            <el-col :span="12" class="switchText">
              <i class="el-icon-view"></i>查看
            </el-col>
          </div>
        </el-row>
      </div>
      <div class="item switchBg">
        <img src="@/assets/code/pic-4.png" />
        <div class="name switchText">工业互联网船舶编码标识规范</div>
        <div class="date switchText">更新时间：2022-03-31</div>
        <el-row class="bottom">
          <div @click="download('http://117.144.170.42:8089/prod-api/profile/pdfs/工业互联网船舶编码标识规范.pdf')">
            <el-col :span="12" class="switchText">
              <i class="el-icon-download"></i>下载
            </el-col>
          </div>
          <div @click="download('http://117.144.170.42:8089/prod-api/profile/pdfs/工业互联网船舶编码标识规范.pdf')">
            <el-col :span="12" class="switchText">
              <i class="el-icon-view"></i>查看
            </el-col>
          </div>
        </el-row>
      </div>
      <div class="item switchBg">
        <img src="@/assets/code/pic-5.png" />
        <div class="name switchText">海关轨迹航信船舶数据项填制规范</div>
        <div class="date switchText">更新时间：2022-03-31</div>
        <el-row class="bottom">
          <div @click="download('http://117.144.170.42:8089/prod-api/profile/pdfs/海关轨迹航信船舶数据项填制规范.pdf')">
            <el-col :span="12" class="switchText">
              <i class="el-icon-download"></i>下载
            </el-col>
          </div>
          <div @click="download('http://117.144.170.42:8089/prod-api/profile/pdfs/海关轨迹航信船舶数据项填制规范.pdf')">
            <el-col :span="12" class="switchText">
              <i class="el-icon-view"></i>查看
            </el-col>
          </div>
        </el-row>
      </div>
      <div class="item switchBg">
        <img src="@/assets/code/pic-6.png" />
        <div class="name switchText">水上施工船舶分类编码</div>
        <div class="date switchText">更新时间：2022-03-31</div>
        <el-row class="bottom">
          <div @click="download('http://117.144.170.42:8089/prod-api/profile/pdfs/水上施工船舶分类编码.pdf')">
            <el-col :span="12" class="switchText">
              <i class="el-icon-download"></i>下载
            </el-col>
          </div>
          <div @click="download('http://117.144.170.42:8089/prod-api/profile/pdfs/水上施工船舶分类编码.pdf')">
            <el-col :span="12" class="switchText">
              <i class="el-icon-view"></i>查看
            </el-col>
          </div>
        </el-row>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      keyword: '',
      list: null,
      listLoading: true
    }
  },
  created() {
  },
  methods: {
    download(_url) {
      window.open(_url, '_target')
    }
  }
}

</script>
<style lang="scss" scoped>
.h-title {
  font-size: 20px;
  line-height: 28px;
  font-weight: 500;
  margin: 0 0 20px;
}

.search {
  height: 88px;
  background-color: #fff;
}

.list {

  overflow: hidden;

  .item {
    margin-top: 24px;
    float: left;
    width: calc(25% - 12px);
    margin-right: 16px;
    height: 290px;
    background-color: #fff;
    border: 1px solid #fff;

    &:nth-child(4n) {
      margin-right: 0;
    }

    img {
      height: 160px;
      width: 100%;
    }

    .name {
      font-size: 16px;
      font-weight: 500;
      color: #000000;
      line-height: 24px;
      margin-left: 23px;
      margin-top: 16px;
    }

    .date {
      font-size: 14px;
      font-weight: 400;
      color: rgb(0, 0, 0, .45);
      line-height: 22px;
      margin-left: 23px;
      margin-top: 10px;
    }

    .bottom {
      margin-top: 14px;
      border-top: 1px dotted #ccc;
      height: 40px;
      line-height: 40px;
      cursor: pointer;

      .el-col {
        text-align: center;
        color: #1A90FE;
        font-size: 14px;

        &:first-child{
          border-right: 1px dotted #ccc;
        }

        i {
          margin-right: 7px;
        }
      }
    }
  }
}

</style>
