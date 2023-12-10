<template>
  <div>
    <div class="header">
      <div class="header-text">
        <NuxtLink to="/spot_list">
          <img src="@/assets/arrow-left.svg" class="back-img">
        </NuxtLink>
      </div>
    </div>
    <h1><span class="title">MyPage</span></h1>
    <div class="around">
      <div style="padding: 10px; margin-bottom: 10px; border: 10px double #E50000; border-radius: 10px;">
        <div class="point_text">
          <span class="point_sentence">現在のポイント:</span>
          <span class="point">00</span>
          <span>pt</span>
        </div>
        <a href="/item_list" class="button"><span>交換可能な商品・サービスを見る</span></a>
      </div>
    </div>
  </div>
</template>
<style scoped>
div {
  text-align: center;
}
.change {
  display: inline-block;
  width: 25vw;
}
.title {
  border-bottom: groove 4px #FF000D;
  width: min(50vw, 100px);
  width: max(50vw, 350px);
}
.around{
  background-color: #FBFFDC;
}
div.point_text{
  font-size:min(6.0vw, 40px);
}
.point_sentence,
.title {
  display: inline-block;
  color: #201F5F;
}
.point_sentence {
  width: min(50vw, 600px);
}
span.point {
  color: #E50000;
  font-weight: bold;
}
.button {
  display: inline-block;
  width: 65vw;
  font-weight: bold;
  padding: 1em 2em;
  color: #fff;
  border-radius: 100vh;
  background: #CC000D;
  background: linear-gradient(0deg, #CC000D 50%, #FFD8DD 100%);
  box-shadow: inset 0 1px 1px rgba(255, 255, 255, .6), 0 5px 10px rgba(0, 0, 0, .1);
  text-decoration: none;
  text-align: center;
  transition: 0.3s;
}
.button:hover {
  background: linear-gradient(0deg, #CC000D 20%, #FFD8DD 100%);
  -webkit-box-shadow: 0 2px 3px rgb(0 0 0 / 10%);
  box-shadow: 0 2px 3px rgb(0 0 0 / 10%);
}

.header {
  display: flex;
  align-items: center;
  justify-content: flex-start;

  height: 40px;
  padding: 4px 8px;

  width: 102%;
  margin-left: -8px;
  margin-top: -8px;

  box-shadow: 0px 2px 6px 0px rgba(0, 0, 0, 0.15);
}
.back-img {
  height: 40px;
  width: 90px;
  margin-top: 7px;
}
</style>
<script>
export default {
  name: 'MyPage'
}
</script>
