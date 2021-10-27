<template>
  <div class="main">
    <!-- <button @click="activities[0].content = '!show'">hhh</button> -->
    <!-- <transition
    appear
    name="animate__animated animate__bounce animate__faster"
    enter-active-class="animate__fadeInLeft"
    leave-active-class="animate__backOutUp">
    <h1 v-show="show">武装起义</h1>
    </transition> -->
    <div class="bg-img1">
      <img src="/static/image/feiniao.png" />
    </div>
    <div class="bg-img2">
      <img src="/static/image/tiananmen.png" />
    </div>
    <div class="event-img">
      <div class="event-img1" @mouseover="Event1">
        <img src="/static/image/xinqingnian.png" />
      </div>
      <div class="event-img2" @mouseover="Event2">
        <img src="/static/image/lidazhao.png" />
      </div>
      <div class="event-img3" @mouseover="Event3">
        <img src="/static/image/wusiyundong.png" />
      </div>
      <div class="event-img4" @mouseover="Event4">
        <img src="/static/image/zhongguoqingnian.png" />
      </div>
    </div>
    <div class="timeline">
      <el-timeline>
        <el-timeline-item
          v-for="(activity, index) in activities"
          :key="index"
          :icon="activity.icon"
          :type="activity.type"
          :color="activity.color"
          :size="activity.size"
          :timestamp="activity.timestamp">
          {{activity.content}}
        </el-timeline-item>
      </el-timeline>
    </div>
  </div>
</template>

<script>
import 'animate.css'
export default {
  name: "wuzhuang",
  data() {
    return {
      show: true,
      activities: [{
          content: '',
          timestamp: '2018-04-12 20:46',
          type: 'danger',
          icon: 'el-icon-circle'
        }, {
          content: '',
          timestamp: '2018-04-03 20:46',
          type: 'danger',
          icon: 'el-icon-circle'
        }, {
          content: '',
          timestamp: '2018-04-03 20:46',
          type: 'danger',
          icon: 'el-icon-circle'
        }, {
          content: '',
          timestamp: '2018-04-03 20:46',
          type: 'danger',
          icon: 'el-icon-circle'
        }]
    };
  },
  methods: {
    Event1: function(){
      this.activities[0].content = '南昌起义';
    }, 
    Event2: function(){
      this.activities[1].content = '八七会议';
    }, 
    Event3: function(){
      this.activities[2].content = '秋收起义';
    }, 
    Event4: function(){
      this.activities[3].content = '井冈山会师';
    }, 
  },
};
</script>

<style lang="less" scoped>
.main {
  width: 80%;
  top: 10%;
  left: 10%;
  height: 80%;
  background-color: antiquewhite;
  border: 5px wheat;
  position: relative;
  //border: 3px solid yellow;
}
.timeline{
    //border: 3px solid blue;
    position: absolute;
    top: 10%;
    left: 75%;
    border: 3px solid blue;
  }
.bg-img1 {
    position:absolute;
    //border: 3px solid blue;
    width: 200px;
  img {
    width: 100%;
  }
}
.bg-img2 {
    //border: 3px solid blue;
    position:absolute;
    width: 200px;
    bottom: 0%;
  img {
    width: 100%;
  }
}
.event-img1 {
    position:absolute;
    top: 20%;
    left: 10%;
    width: 300px;
  z-index: 4;
  img {
    width: 100%;
  }
}
.event-img2 {
    position:absolute;
    top: 30%;
    left: 20%;
    width: 300px;
  z-index: 3;
  img {
    width: 100%;
  }
}
.event-img3 {
    position:absolute;
    top: 40%;
    left: 30%;
    width: 300px;
  z-index: 2;
  img {
    width: 100%;
  }
}
.event-img4 {
    position:absolute;
    top: 50%;
    left: 40%;
    width: 300px;
  z-index: 1;
  img {
    width: 100%;
  }
}
.event-img1,.event-img2,.event-img3,.event-img4 {

transition:All 0.4s ease-in-out;

-webkit-transition:All 0.4s ease-in-out;

-moz-transition:All 0.4s ease-in-out;

-o-transition:All 0.4s ease-in-out;

}

.event-img1:hover,.event-img2:hover,.event-img3:hover,.event-img4:hover {

transform:scale(1.2);

-webkit-transform:scale(1.2);

-moz-transform:scale(1.2);

-o-transform:scale(1.2);

-ms-transform:scale(1.2);
animation:myfirst 2s;
	-webkit-animation:myfirst 2s;
z-index: 5;

}
@keyframes myfirst
{
	50%  {left:30%; top:30%;}
	100%  {left:30%; top:30%;}
}

@-webkit-keyframes myfirst /* Safari and Chrome */
{
	50%  {left:30%; top:30%;}
	100%  {left:30%; top:30%;}
}
</style>