<template>
	<div class="table-line">
    <table>
      <tr>
        <th>
          <div class="line-box">  
            <table>  
              <thead>  
                <tr>  
                  <th></th>  
                  <th>等级告警</th>  
                </tr>  
                <tr>  
                  <th>资产保障等级</th>  
                  <th></th>  
                </tr>  
              </thead>  
            </table>  
          </div>  
        </th>
        <th>严重告警</th>
        <th>严重告警</th>
      </tr>
      <tr>
        <td>一级保障</td>
        <td>
          <el-select v-model="value" placeholder="请选择"> 
            <el-option
              v-for="item in options"
              :key="item.value"
              :label="item.label"
              :value="item.value">
            </el-option>
          </el-select> 
        </td>
        <td>
          <el-select v-model="value" placeholder="请选择"> 
            <el-option
              v-for="item in options"
              :key="item.value"
              :label="item.label"
              :value="item.value">
            </el-option>
          </el-select> 
        </td>
      </tr>
    </table>
  </div>
</template>

<script>
export default{
  data () {
    return {
      options: [{
        value: '选项1',
        label: '呵呵'
      }, {
        value: '选项2',
        label: '哈哈'
      }, {
        value: '选项3',
        label: '嘿嘿'
      }, {
        value: '选项4',
        label: '格格'
      }
      ],
      value: '选项1'
    }
  },
  methods: {
  },
  mounted () {
  }
}
</script>

<style lang="less">
.table-line{
  width:600px;
  height:500px;
  table{
    width: 100%;
    font-size:12px;
    border-width: 1px;
    border-color: #666666;
    border-collapse: collapse;
    th{
      border-width: 1px;
      padding: 2px;
      border-style: solid;
      border-color: #666666;
      .line-box{
        background-image: url(./line0.png);
        background-size: 100% 100%;
        table{
          width: 100%
        }
        th{
          border: none;
        }
      }
    }
    td {
      border-width: 1px;
      padding: 8px;
      border-style: solid;
      border-color: #666666;
      background-color: #ffffff;
    }
  }
}
</style>