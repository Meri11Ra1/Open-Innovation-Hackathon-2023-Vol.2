<template>
  <div>
    <div class="spot-row">
      <img :src="{icon}">
      {{ icon }}
      <div class="spot-congestion" :class="{'congestion-high': spotData.congestion == '混雑', 'congestion-row': spotData.congestion == '空き'}">{{ spotData.congestion }}</div>
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
    spotData: Object,
    icon: String
  }
}
</script>

<style>
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
    writing-mode: vertical-rl;
    text-orientation: upright;

    margin-right: 12px;
  }
  .congestion-high {
    color: #ff4c4c;
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
  }
  .spot-address {
    margin-top: 3px;
    font-size: 12px;
  }
}
</style>
