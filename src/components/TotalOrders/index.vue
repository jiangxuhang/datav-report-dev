<template>
  <common-card title="累计订单量" value="￥241352462">
    <template>
      <div id="total-orders-chart" :style="{width:'100%', height:'100%'}"></div>
    </template>
    <template #footer>
      <span>昨日订单量</span>
      <span class="emphasis">2000000</span>
    </template>
  </common-card>
</template>
<script>
import commonCardMixin from '../../mixins/commonCardMixin'
export default {
  mixins: [commonCardMixin],
  mounted() {
    const chartDom = document.getElementById('total-orders-chart')
    const chart = this.$echarts.init(chartDom)
    chart.setOption({
      xAxis: {
        type: 'category',
        show: false,
        boundaryGap: false
      },
      yAxis: {
        show: false
      },
      series: [{
        type: 'line',
        areaStyle: {
          color: 'purple'
        },
        lineStyle: {
          width: 0
        },
        itemStyle: {
          opacity: 0
        },
        smooth: true,
        data: [620, 432, 220, 113, 556, 234, 553, 123, 643, 321, 124, 643]
      }],
      grid: {
        top: 0,
        bottom: 0,
        right: 0,
        left: 0
      }
    })
  }
}
</script>
<style lang="scss">
</style>
