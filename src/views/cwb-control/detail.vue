<template>
  <div class="app-container">
    <div class="h-title switchText">设备详情</div>
    <div class="main switchBg">
      <div class="part">
        <el-row>
          <el-col :span="4">
            <div class="title switchText">基本信息</div>
          </el-col>
          <el-col :span="2" :offset="18" class="tr">
            <el-button size="small" type="primary">编辑</el-button>
          </el-col>
        </el-row>
        <el-row>
          <el-col :span="6">
            <div class="item">
              <span class="item-lable switchText">设备编号:</span>
              <span class="item-c switchText">BH23423423</span>
            </div>
          </el-col>
          <el-col :span="6">
            <div class="item">
              <span class="item-lable switchText">设备名称:</span>
              <span class="item-c switchText">空压机#01</span>
            </div>
          </el-col>
          <el-col :span="6">
            <div class="item">
              <span class="item-lable switchText">设备厂商:</span>
              <span class="item-c switchText">英格索兰</span>
            </div>
          </el-col>
          <el-col :span="6">
            <div class="item">
              <span class="item-lable switchText">设备类型:</span>
              <span class="item-c switchText">船坞泵</span>
            </div>
          </el-col>
          <el-col :span="6">
            <div class="item">
              <span class="item-lable switchText">设备型号:</span>
              <span class="item-c switchText">JS2341</span>
            </div>
          </el-col>
          <el-col :span="6">
            <div class="item">
              <span class="item-lable switchText">是否支持反控:</span>
              <span class="item-c switchText">是</span>
            </div>
          </el-col>
          <el-col :span="6">
            <div class="item">
              <span class="item-lable switchText">负责人:</span>
              <span class="item-c switchText">封欢</span>
            </div>
          </el-col>
          <el-col :span="6">
            <div class="item">
              <span class="item-lable switchText">出厂日期:</span>
              <span class="item-c switchText">2018-02-14</span>
            </div>
          </el-col>
          <el-col :span="6">
            <div class="item">
              <span class="item-lable switchText">调试日期:</span>
              <span class="item-c switchText">2018-02-16</span>
            </div>
          </el-col>
          <el-col :span="6">
            <div class="item">
              <span class="item-lable switchText">采集网管:</span>
              <span class="item-c switchText">D2493435</span>
            </div>
          </el-col>
          <el-col :span="6">
            <div class="item">
              <span class="item-lable switchText">备注:</span>
              <span class="item-c switchText">34059820383204</span>
            </div>
          </el-col>
        </el-row>
      </div>
      <div class="part">
        <el-row>
          <el-col :span="4">
            <div class="title switchText">采集配置</div>
          </el-col>
          <el-col :span="2" :offset="18" class="tr">
            <el-button size="small" type="primary">编辑</el-button>
          </el-col>
        </el-row>
        <el-row>
          <el-col :span="6">
            <div class="item">
              <span class="item-lable switchText">模版名称:</span>
              <span class="item-c switchText">Test demo 001</span>
            </div>
          </el-col>
          <el-col :span="6">
            <div class="item">
              <span class="item-lable switchText">模板描述:</span>
              <span class="item-c switchText">英格索兰</span>
            </div>
          </el-col>
          <el-col :span="6">
            <div class="item">
              <span class="item-lable switchText">驱动类型:</span>
              <span class="item-c switchText">ModBus_RTU</span>
            </div>
          </el-col>
          <el-col :span="6">
            <div class="item">
              <span class="item-lable switchText">采集间隔:</span>
              <span class="item-c switchText">25 ms</span>
            </div>
          </el-col>
          <el-col :span="6">
            <div class="item">
              <span class="item-lable switchText">采集超时:</span>
              <span class="item-c switchText">2000 ms</span>
            </div>
          </el-col>
          <el-col :span="6">
            <div class="item">
              <span class="item-lable switchText">重试次数:</span>
              <span class="item-c switchText">3</span>
            </div>
          </el-col>
          <el-col :span="6">
            <div class="item">
              <span class="item-lable switchText">串口号:</span>
              <span class="item-c switchText">COM2</span>
            </div>
          </el-col>
          <el-col :span="6">
            <div class="item">
              <span class="item-lable switchText">站号:</span>
              <span class="item-c switchText">1</span>
            </div>
          </el-col>
          <el-col :span="6">
            <div class="item">
              <span class="item-lable switchText">波特率:</span>
              <span class="item-c switchText">19200</span>
            </div>
          </el-col>
          <el-col :span="6">
            <div class="item">
              <span class="item-lable switchText">数据位:</span>
              <span class="item-c switchText">8</span>
            </div>
          </el-col>
          <el-col :span="6">
            <div class="item">
              <span class="item-lable switchText">停止位:</span>
              <span class="item-c switchText">1</span>
            </div>
          </el-col>
          <el-col :span="6">
            <div class="item">
              <span class="item-lable switchText">校验:</span>
              <span class="item-c switchText">无校验</span>
            </div>
          </el-col>
        </el-row>
      </div>
    </div>
  </div>
</template>
<script>
import { getEquDwList } from '@/api/table'
import Pagination from '@/components/Pagination'

export default {
  components: { Pagination },
  filters: {
    statusFilter(status) {
      const statusMap = {
        published: 'success',
        draft: 'info',
        deleted: 'danger'
      }
      return statusMap[status]
    },
    isFkFilter(isFk) {
      if (isFk === 1) {
        return '是'
      } else {
        return '否'
      }
    }
  },
  data() {
    return {
      list: null,
      listLoading: true,
      total: 0,
      listQuery: {
        page: 1,
        limit: 20
      },
      dialogFormVisible: false,
      dialogStatus: '',
      rules: {
        type: [{ required: true, message: '请选择设备类型', trigger: 'change' }],
        name: [{ required: true, message: '请输入设备名称', trigger: 'blur' }],
      },
      id: this.$route.params.id
    }
  },
  created() {
    this.fetchData()
  },
  methods: {
    fetchData() {
      this.listLoading = true
      getEquDwList(this.listQuery).then(response => {
        this.list = response.data.items
        this.listLoading = false
        this.total = response.data.total
      })
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

.tr {
  text-align: right;
}

.main {
  background-color: #FFF;
  padding: 24px;
  min-height: 70vh;

  .part {
    &:not(:first-child) {
      margin-top: 30px;
    }

    &:last-child {
      padding-bottom: 20px;
      border-bottom: 1px solid rgba(0, 0, 0, .06);
    }

    .title {
      font-size: 16px;
      color: rgba(0, 0, 0, 0.85);
      line-height: 24px;
      font-weight: 500;
    }

    .item {
      margin-top: 16px;

      .item-lable {
        font-size: 14px;
        line-height: 22px;
        color: rgba(0, 0, 0, 0.85);
      }

      .item-c {
        font-size: 14px;
        line-height: 22px;
        color: rgba(0, 0, 0, 0.65);
        margin-left: 5px;
      }
    }
  }

  .table-title {
    font-size: 16px;
    font-weight: 500;
    color: #000000;
    line-height: 24px;
    margin: 20px 0;
  }
}

.form {
  background-color: #fff;
  height: 80px;

  .el-col {
    margin-top: 20px;
  }
}

.table-wrap {
  background-color: #fff;
  padding: 16px;

  .el-button {
    margin-bottom: 16px;
  }
}

.el-dialog__body .filter-item {
  width: 280px;
}
.theme-dark .main .part:last-child{
  border-bottom-color: #fff;
}
</style>
