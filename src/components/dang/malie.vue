<template>
  <div class="main">
    <div class="title">
      <img class="text" src="/static/image/title-malie.png" />
      <img src="/static/image/icon-boat.png" class="icon" />
    </div>
    
<!-- 标题下面的下划线 -->
    <div class="bg-line"></div>
<!-- 时间轴的基线 -->
    <!-- <div class="line"></div> -->

    <!-- 背景3/4圆 -->
    <div class="circle">
      <div class="bg-circle">
        <img src="/static/image/circle.png" />
      </div>
      <!-- 圆上的点 -->
      <div class="dot-circle">
        <div class="first-dot" v-on:click = "show1 = true; show2 = false; show3 = false; show4 = false">
          <img src="/static/image/dot.png" />
        </div>
        <div class="second-dot" v-on:click = "show1 = false; show2 = true; show3 = false; show4 = false">
          <img src="/static/image/dot.png" />
        </div>
        <div class="third-dot" v-on:click = "show1 = false; show2 = false; show3 = true; show4 = false">
          <img src="/static/image/dot.png" />
        </div>
        <div class="forth-dot" v-on:click = "show1 = false; show2 = false; show3 = false; show4 = true">
          <img src="/static/image/dot.png" />
        </div>
      </div>
    </div>
    <transition name = "fade">
    <div v-show = "show1" class="first">
      <div class="time">1915.09</div>
      <div class="para">《新青年》杂志创刊</div>
      <div class="event-img">
        <img src="/static/image/xinqingnian.png" />
      </div>
    </div>
    </transition>
    <transition name = "fade">
    <div v-show = "show2" class="second">
      <div class="time">1918.07</div>
      <div class="para">
        <div>《法俄革命之比较观》</div>
        <div>《庶民的胜利》</div>
        <div>《Bolshevism的胜利》</div>
      </div>
      <div class="event-img">
        <img src="/static/image/lidazhao.png" />
      </div>
    </div>
    </transition>
    <transition name = "fade">
    <div v-show = "show3" class="third">
      <div class="time">1919.05</div>
      <div class="para">五四运动</div>
      <div class="event-img">
        <img src="/static/image/wusiyundong.png" />
      </div>
    </div>
    </transition>
    <transition name = "fade">
      <div v-show = "show4" class="forth">
        <div class="time">1923.10</div>
        <div class="para">《中国青年》周刊创办</div>
        <div class="event-img">
          <img src="/static/image/zhongguoqingnian.png" />
        </div>
      </div>
    </transition>
  </div>
</template>

<script>
export default {
    name:'malie',
  data() {
    return {
      show1: true,
      show2: false,
      show3: false,
      show4: false,
    }
  },
  methods: {},
};
</script>

<style lang="less" scoped>
.main {
  position: relative;
}

.title {
  position: relative;
  left: 3%;
  padding-top: 1%;
  width: 400px;
  display: flex;
  .text {
    width: 82%;
  }
  .icon {
    width: 12%;
    height: 12%;
  }
}
// 标题下面的下划线
.bg-line {
  border-bottom: 2px solid #ffe699;
  width: 400px;
  margin-top: -25px;
  margin-left: 3%;
}

// 时间轴的基线
.line {
  border-top: 3px solid #ffe699;
  height: 0;
  width: 80%;
  margin: 0 auto;
  position: absolute;
  top: 250px;
  left: 10%;
}

@begin-left: 100px;

@begin-top: 100px;

.first,.second,.third,.forth {
  position: absolute;
  .time{
    font-size: 5em;
    position:absolute;
    top: @begin-top;
    left: @begin-left;
  }
  .para{
    font-size: 1.5em;
    position:absolute;
    top: @begin-top+100%;
    left: @begin-left;
    width: 240px;
  }
  .event-img {
      position:absolute;
      top: 40px;
      left: 400px;
      width: 420px;
    img {
      width: 100%;
    }
  }
  color:antiquewhite;
}

.circle{
  margin-left: 53%;
  top: 10%;
  position: absolute;
  // border: 3px solid blue;
}
.bg-circle{
  z-index: 1;
  img {
    height: 540px;
  }
}
.dot-circle{
  .first-dot{
      left: 30%;
      top: 3%;
      position: absolute;
      z-index: 2;
      img {
        height: 20px;
      }
  }
  .second-dot{
      left: 77%;
      top: 12%;
      position: absolute;
      z-index: 2;
      img {
        height: 20px;
      }
  }
  .third-dot{
      left: 77%;
      top: 77%;
      position: absolute;
      z-index: 2;
      img {
        height: 20px;
      }
  }
  .forth-dot{
      left: 30%;
      top: 86%;
      // border: 1px solid black;
      position: absolute;
      z-index: 2;
      img {
        height: 20px;
      }
  }
}
.fade-enter-active, .fade-leave-active {
    transition: opacity 2s
}
.fade-enter, .fade-leave-to /* .fade-leave-active, 2.1.8 版本以下 */ {
    opacity: 0
}
</style>