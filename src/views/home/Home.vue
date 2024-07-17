<template>
<!--  <h2>首页</h2>-->
  <div id="main" style="width: 600px;height:400px;"></div>
</template>

<script>
import * as echarts from 'echarts';
export default {
  mounted() {
    // 基于准备好的dom，初始化echarts实例
    var myChart = echarts.init(document.getElementById('main'));
// 指定图表的配置项和数据
    var option = {
      title: {
        text: '丢坤个人数值'
      },
      tooltip: {},
      legend: {
        data: ['综合能力']
      },
      xAxis: {
        data: ['扯犊', '喝酒', '体能', '瞌睡']
      },
      yAxis: {},
      series: [
        {
          name: '综合能力',
          type: 'bar',
          data: [99, 101, 77, 88]
        }
      ]
    };
// 使用刚指定的配置项和数据显示图表。
    myChart.setOption(option);
  }
}
</script>

<style scoped>

</style>