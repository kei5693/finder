<template>
  <div class="intro">
    <div id="introCont" :class="{ 'on': popUpClose }">
      <div class="left">
        <div @click="closePopUP()"><img src="@/assets/images/text_intro01.png" alt="찾고 싶은 콘텐츠가 있으신가요? 검색도우미 Finder를 사용해보세요!"></div>
      </div>
      <div class="right"><a href="#" target="_blank">페이지 이동</a></div>
    </div>
  </div>
</template>
<script>
export default {
  data(){
    return {
      popUpClose: false,
    }
  },
  methods: {
    closePopUP(){
      this.popUpClose = !this.popUpClose;
    }
  },
}
</script>
<style>
html, body, #app {
  height:100%;
}
.intro {
  height:100%;
  background: url('~@/assets/images/bg_dummy.png') no-repeat;
  background-size: 100% auto;
}
#introCont {
  position: absolute;
  bottom:16%;
  right:10px;
  width:calc(100% - 20px);
  height:62px;
  background: #FF6600;
  border-radius: 20px;
  text-align: left;
}
#introCont.on {
  animation: close_step01 0.5s forwards;
}
#introCont > .left {
  overflow: hidden;
  position: relative;
  width: 100%;
  height: 100%;
}
#introCont > .left > div {
  margin: 12px 50px 0 12px;
}
#introCont > .left > div > img {
  height:38px;
}
#introCont > .right {
  position: absolute;
  bottom:0;
  right:-2px;
}
#introCont > .right > a,
#introCont > .right:after {
  background: url('~@/assets/images/sp_index.png') no-repeat;
  background-size: 1000px 1000px;
  font-size:0;
  line-height:0;
  text-indent:-9999px;
  color:transparent;
}
#introCont > .right > a {
  display:inline-block;
  position:relative;
  z-index:500;
  width:42px;
  height:42px;
  background-position: 0 0;
}
#introCont > .right:after {
  content:'';
  position: absolute;
  top:5px;
  right:7px;
  width:18px;
  height:15px;
  background-position: -75px 0;
  }
#introCont.on > .right:after {
  animation-name: close_step02, close_step03;
  animation-iteration-count: 1, infinite;
  animation-direction: normal, alternate;
  animation-duration: 0.5s, 1s;
  animation-fill-mode: forwards;
  animation-delay: 1s, 2s;
}

@keyframes close_step01{
  0%, 30% {height:62px;}
  100%    {width:40px;height:40px;}
}
@keyframes close_step02{
  0%    {top:5px;right:7px;}
  60%   {top:-18px;right:0;}
  100%  {top:-12px;right:0;}
}
@keyframes close_step03{
  0%,30%    {top:-12px;right:0;}
  50%,100%  {top:-15px;right:0;}
}
</style>