<template>
  <div class="map-view">
    <div class="left">
      <b-map-scatter></b-map-scatter>
    </div>
    <div class="right">
      <el-card shadow="hover">
        <template #header>
          <div class="title">
            用户月同比增长
          </div>
        </template>
        <template>
          <div class="chart-wrapper">
            111
          </div>
        </template>
      </el-card>
      <el-card shadow="hover">
        <template #header>
          <div class="title">
            热门搜索
          </div>
        </template>
        <template>
          <div class="chart-wrapper">
            111
          </div>
        </template>
      </el-card>
    </div>
  </div>
</template>
<script>
import BMapScatter from '../BMapScatter'
export default {
  components: { BMapScatter }
}
</script>
<style lang="scss" scoped>
.map-view {
  display: flex;
  margin-top: 20px;
  .left {
    flex: 0 0 80%;
    width: 80%;
    height: 600px;
    background: #fff;
  }
  .right {
    flex: 1;
    display: flex;
    flex-direction: column;
    margin-left: 20px;
    justify-content: space-between;
    .title {
      display: flex;
      align-items: center;
      height: 60px;
      box-sizing: border-box;
      border-bottom: 1px solid #eee;
      font-size: 14px;
      font-weight: 500;
      padding: 0 0 0 20px;
    }
    .chart-wrapper {
      width: 100%;
      height: 190px;
    }
  }
}
</style>
