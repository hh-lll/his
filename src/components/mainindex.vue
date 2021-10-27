<template>
  <div class="main">
    <div class="title">{{ msg }}</div>
    <div class="clock">
      <div class="desc">时至今日，中国共产党成立已有</div>
      <Clock />
    </div>
    <div class="para">
      <div class="each_p">2021年是中国共产党建党100周年</div>
      <div class="each_p">100年的砥砺筑梦</div>
      <div class="each_p">一路风雨一路歌</div>
      <div class="each_p">一路拼搏一路唱</div>
      <div class="each_p">一路坎坷一路颂</div>
      <div class="each_p">一路跋涉一路咏</div>
      <div class="each_p">一路凯歌一路舞</div>
      <div class="each_p">中国共产党人始终以初心为桨、借时代之舟、化使命为帆，砥砺前行</div>
    </div>
  </div>
</template>

<script>
import Clock from "./clock.vue";

export default {
  name: "mainindex",
  data() {
    return {
      msg: "百年征程波澜壮阔，百年初心历久弥坚",
    };
  },
  components: {
    Clock,
  },
};
</script>

<style lang="less" scoped>
@head_color: #FFE699;
@p_color:#FFE699;
.main {
  text-align: center;
  font-family: playfairdisplay-bold, playfair display, serif;
  width: 100%;
  // color: white;
}

.title {
  font-size: 4.5em;
  margin: 50px 0;
  height: 50px;
  color:@head_color;
  font-family: "STXingkai";
}

.desc {
  font-size: 1.8em;
  padding-bottom: 10px;
  color:@head_color;
}

.clock {
  width: 45%;
  margin: 0 auto;
  color:antiquewhite;
}
.para{
  color:@p_color;
  font-size: 1.5em;
  .each_p{
    padding-bottom: 6px;
  }
}
</style>