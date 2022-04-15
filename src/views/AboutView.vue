<template>
  <div class="about">
    <div id="main" style="width: 600px;height: 400px;"></div>
  </div>
</template>
<script>
export default {
  name: 'Echarts',
  methods: {
    myEcharts(){
      var myChart = this.$echarts.init(document.getElementById('main'));
      //配置图表
      var option = {
        xAxis: {
          type: 'category',
          data: ['Mon', 'Tue', 'Wed', 'Thu', 'Fri', 'Sat', 'Sun']
          },
          yAxis: {
            type: 'category',
            // data:[-204, -136, -68, 68, 136, 204]
          },
          series: [
            {
              data: [
            2.0,
            -2.0,
            1.0,
            3.0,
            -3.0,
            0.0,
            -100.0,
            -101.0,
            -102.0,
            100.0,
            101.0,
            102.0,
            -10.0,
            -11.0,
            -12.0,
            -10.0,
            -101.0,
            -12.0,
            -1.0,
            -10.0,
            -2.0,
            10.0,
            1.0,
            102.0,
            111.0,
            112.0,
            113.0,
            100.0,
            101.0,
            102.0
          ],
              type: 'line'
            }
          ]
      };
      myChart.setOption(option);
    }
  },
  mounted(){
    this.myEcharts();
  }
}
</script>