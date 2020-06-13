<template>
  <common-card title="累计销售额" value="￥32141352462">
    <template>
      <div class="compare">

      </div>
    </template>
    <template #footer>
      <span>昨日销售额</span>
      <span class="money">￥3000000</span>
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
span {
  font-size: 12px;
}
.compare {
  height: 100%;
  background: yellow;
}
.money {
  margin-left: 5px;
  color: #333;
  font-weight: 700;
}
</style>
