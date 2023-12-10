<template>
  <div>
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
        { id: 4, congestion: '普通', name: '陶芸JIN', address: '島尻郡与那原町板良敷847−3', icon: NormalIcon }
      ]
    }
  }
}
</script>
