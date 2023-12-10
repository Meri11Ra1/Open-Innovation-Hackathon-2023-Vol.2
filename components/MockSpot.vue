<template>
  <div class="mock-spot">
    <div class="spot-row">
      <div class="vertical-box icon-box">
        <img :src="spotData.icon" class="icon-img">
        <div class="spot-congestion" :class="{'congestion-high': spotData.congestion == '混雑', 'congestion-row': spotData.congestion == '空き', 'congestion-normal': spotData.congestion == '普通'}">{{ spotData.congestion }}</div>
      </div>
      <div class="vertical-box">
        <div class="spot-name">
          {{ spotData.name }}
        </div>
        <div class="spot-address">
          {{ spotData.address }}
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    spotData: Object
  }
}
</script>

<style scoped>
.spot-row {
  border-top: 1px solid rgba(121, 116, 126, 0.16);
  border-bottom: 1px solid rgba(121, 116, 126, 0.16);

  padding: 12px;

  display: flex;
  align-items: center;

  overflow: hidden;
  color:#4A6366;
  text-overflow: ellipsis;

  .spot-congestion {
    margin-top: -10px;
    margin-left: -2px;
  }
  .congestion-high {
    color: #ff5454;
  }
  .congestion-normal {
    color: #FF9347;
  }
  .congestion-row {
    color: #4747ff;
  }
  .vertical-box {
    display: flex;
    flex-flow: column;
  }
  .spot-name {
    font-size: 16px;
    font-style: normal;
    font-weight: 600;
    line-height: 20px;
    letter-spacing: 0.1px;

    margin-top: 10px;
  }
  .spot-address {
    margin-top: 3px;
    font-size: 12px;
  }
  .icon-box {
    text-align: center;
    margin-right: 20px;
  }
  .icon-img {
    width: 50px;
    height: 50px;
    color: red;
  }
}
</style>
