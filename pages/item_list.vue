<template>
  <div>
    <h1>
      交換品一覧
    </h1>
  </div>
</template>

<script>
export default {
  data () {
    return {
      itemList: [
        { id: 1, congestion: '混雑', name: '美ら海水族館', address: '国頭郡本部町石川424' },
        { id: 2, congestion: '普通', name: 'エイサー会場', address: '諸見里2丁目1-1' },
        { id: 3, congestion: '空き', name: '琉球ガラス村', address: '糸満市福地169' },
        { id: 4, congestion: '普通', name: '陶芸JIN', address: '島尻郡与那原町板良敷847−3' }
      ]
    }
  }
}
</script>

<style>
h1 {
  text-align: center;
}

p, button , label{
  font-size: 4.5vw;
}

button {
  width: 50%;
  border: none;
  border-radius: 3vh;
  background-color: rgb(54, 155, 255);
  color: white;
  padding: 1.5vh;
}

</style>
