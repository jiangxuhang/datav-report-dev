<template>
  <common-card title="累计订单量" value="￥241352462">
    <template>
      <v-chart :options="getOptions()"></v-chart>
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
  methods: {
    getOptions() {
      return {
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
      }
    }
  },
  mounted() {
  }
}
</script>
<style lang="scss">
</style>
