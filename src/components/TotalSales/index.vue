<template>
  <common-card title="累计销售额" value="￥32141352462">
    <template>
      <div class="compare-wrapper">
        <div class="compare">
          <span>日同比</span>
          <span class="emphasis">7.33%</span>
          <div class="increase"></div>
        </div>
        <div class="compare">
          <span>月同比</span>
          <span class="emphasis">38.79%</span>
          <div class="decrease"></div>
        </div>
      </div>
    </template>
    <template #footer>
      <span>昨日销售额</span>
      <span class="emphasis">￥3000000</span>
    </template>
  </common-card>
</template>
<script>
import commonCardMixin from '../../mixins/commonCardMixin'
export default {
  mixins: [commonCardMixin]
}
</script>
<style lang="scss" scoped>
.compare-wrapper {
  display: flex;
  flex-direction: column;
  height: 100%;
  justify-content: center;
  .compare {
    font-size: 12px;
    margin-top: 3px;
    color: #666;
    display: flex;
    align-items: center;
  }
}
</style>
