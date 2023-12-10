<template>
  <div class="spot-list">
    <div class="header">
      <div class="header-text">
        <NuxtLink to="/my_page">マイページ</NuxtLink>
      </div>
    </div>
    <div v-for="spot in spotList" :key="spot.id">
      <mock-spot :spot-data="spot" :icon="spot.icon" />
    </div>
  </div>
</template>
<script>
import HighIcon from '../assets/high.svg'
import NormalIcon from '../assets/normal.svg'
import LowIcon from '../assets/low.svg'
export default {
  data () {
    return {
      spotList: [
        { id: 1, congestion: '混雑', name: '美ら海水族館', address: '国頭郡本部町石川424', icon: HighIcon },
        { id: 2, congestion: '普通', name: 'エイサー会場', address: '諸見里2丁目1-1', icon: NormalIcon },
        { id: 3, congestion: '空き', name: '琉球ガラス村', address: '糸満市福地169', icon: LowIcon },
        { id: 4, congestion: '普通', name: '陶芸JIN', address: '島尻郡与那原町板良敷847−3', icon: NormalIcon },
        { id: 5, congestion: '混雑', name: '美ら海水族館', address: '国頭郡本部町石川424', icon: HighIcon },
        { id: 6, congestion: '普通', name: 'エイサー会場', address: '諸見里2丁目1-1', icon: NormalIcon },
        { id: 7, congestion: '空き', name: '琉球ガラス村', address: '糸満市福地169', icon: LowIcon },
        { id: 8, congestion: '普通', name: '陶芸JIN', address: '島尻郡与那原町板良敷847−3', icon: NormalIcon },
        { id: 9, congestion: '混雑', name: '美ら海水族館', address: '国頭郡本部町石川424', icon: HighIcon },
        { id: 10, congestion: '普通', name: 'エイサー会場', address: '諸見里2丁目1-1', icon: NormalIcon },
        { id: 11, congestion: '空き', name: '琉球ガラス村', address: '糸満市福地169', icon: LowIcon },
        { id: 12, congestion: '普通', name: '陶芸JIN', address: '島尻郡与那原町板良敷847−3', icon: NormalIcon }
      ]
    }
  }
}
</script>

<style>
.header {
  display: flex;
  align-items: center;
  justify-content: flex-end;

  height: 40px;
  padding: 4px 8px;

  width: 102%;
  margin-left: -8px;
  margin-top: -8px;

  box-shadow: 0px 2px 6px 0px rgba(0, 0, 0, 0.15);
}
.header-text {
  margin-right: 15px;
}
</style>
