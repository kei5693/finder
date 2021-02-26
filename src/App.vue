<template>
  <div id="app">
    <router-view/>
  </div>
</template>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: left;
  color: #2c3e50;
}

#nav {
  padding: 30px;
}

#nav a {
  font-weight: bold;
  color: #2c3e50;
}

#nav a.router-link-exact-active {
  color: #42b983;
}




html, body, #app, #contentBox {
  height:100%;
}
#contentBox {
  position: relative;
  height:100%;
  /* background: #ebf0f3; */
}
#contentBox #header {
  position: fixed;
  top:0;
  left:0;
  z-index: 100;
  width:100%;
  padding:0 18px;
  background: #ebf0f3;
  box-sizing: border-box;
}
#contentBox #header > div {
  position: relative;
  display:flex;
  height:50px;
  justify-content: flex-end;
  align-items: center;
}
#contentBox #header > div:after {
  content:'';
  position: absolute;
  top:50%;
  left:0;
  width:68px;
  height:20px;
  background:url('~@/assets/images/sp_index.png') no-repeat 0 -100px;
  background-size: 1000px 1000px;
  transform: translateY(-50%);
}
#contentBox #header > div button {
  border:0 none;
  font-size:0;
  line-height:0;
  text-indent:-9999px;
  width:43px;
  height:24px;
  background:url('~@/assets/images/sp_index.png') no-repeat;
  background-position: -100px -100px;
  background-size: 1000px 1000px;
}
#contentBox #header > div button + button {
  width:79px;
  margin-left:10px;
  background-position: -200px -100px;
}
#contentBox #content {
  height:100%;
  padding:50px 0;
  box-sizing: border-box;
  background: #ebf0f3;
}
#contentBox #content .visual {
  display:flex;
  align-items: center;
  height:100%;
}
#contentBox #content .visual > div {
  position: relative;
  max-width:720px;
  margin:0 auto;
  background: #ebf0f3;
  overflow:hidden;
}
#contentBox #content .visual > div > img:first-child {
  position: static;
}
#contentBox #content .visual > div > img,
#contentBox #content .visual > div > div {
  position: absolute;
  top:0;
  left:0;
  width:100%;
}
#contentBox #content .visual > div img.img01 {
  opacity: 0;
  margin-left:-10%;
}
#contentBox #content .visual > div img.img02 {
  top:100%;
  z-index: 200;
}
#contentBox #content .visual > div > div > img {
  width:50%;
  position: absolute;
  top: 0;
  opacity: 0;
}
#contentBox #content .visual > div > div img.img0301 {
  left:0;
  transform-origin: 63.33% 87.22%;
  margin:2% 0 0 5%;
  transition: all 0.5s;
}
#contentBox #content .visual > div > div img.img0302 {
  right:0;
  transform-origin: 39.44% 69.34%;
  margin:4% 4% 0 0;
  transition: all 0.5s;
}
#contentBox #content .visual > div img.img04 {
  transform:scale(0);
  transform-origin: 50% 100%;
}
#contentBox #content .visual.on > div img.img01 {
  animation: aniSlideLeft 0.5s ease forwards;
}
#contentBox #content .visual.on > div img.img02 {
  animation: aniSlideTop 0.6s cubic-bezier(0.5, 0, 0.5, 1.5) forwards;
  animation-delay: 0.3s;
}
#contentBox #content .visual.on > div img.img0301 {
  opacity: 1;
  margin:0;
  transition-delay: 1s;
}
#contentBox #content .visual.on > div img.img0302 {
  opacity: 1;
  margin:0;
  transition-delay: 1.3s;
}
#contentBox #content .visual.on > div img.img04 {
  animation-name: aniScale, aniScaleLoop;
  animation-duration:1s, 4s;
  animation-timing-function:cubic-bezier(0.8, 0, 0.5, 1.8), linear;
  animation-fill-mode: forwards;
  animation-iteration-count: 1, infinite;
  animation-delay: 1.5s, 6s;
}
@keyframes aniSlideLeft {
  0%        {opacity: 0;margin-left:-10%;}
  80%,100%  {opacity: 1;margin-left:0;}
}
@keyframes aniSlideTop {
  0%    {top:100%;}
  100%  {top:0%;}
}
@keyframes aniScale {
  0%    {transform:scale(0);}
  100%  {transform:scale(1);}
}
@keyframes aniScaleLoop {
  0%        {transform:scale(1);}
  4%        {transform:scale(1.2);}
  8%        {transform:scale(1);}
  12%       {transform:scale(1.2);}
  16%,100%  {transform:scale(1);}
}
#contentBox #content .productPick {
  overflow-y:scroll;
  position: fixed;
  top:0;
  left:100%;
  z-index: 200;
  width:100%;
  height:100%;
  background: greenyellow;
  transition:left 0.5s ease;
}
#contentBox #content .productPick.on {
  left:0;
}
#contentBox #searchBox {
  position: fixed;
  bottom:0;
  left:0;
  z-index: 999;
  width:100%;
  height:50px;
}
#contentBox #searchBox .searchInput {
  position: relative;
  z-index: 200;
  display: flex;
  align-items: center;
  height:100%;
  background:#fff;
  border-radius: 18px 18px 0 0;
  box-sizing: border-box;
  transition: border-radius 0.3s;
}
#contentBox #searchBox.on .searchInput{
  border-radius: 0 0 0 0;
  border-top: 1px solid #ebebeb;
}
#contentBox #searchBox .searchInput > div {
  display: grid;
  grid-template-columns: 34px auto 34px;
  grid-column-gap: 10px;
  width: 100%;
  height: 34px;
  padding: 0 18px;
  box-sizing: border-box;
}
#contentBox #searchBox .searchInput > div > button {
  width:34px;
  height:34px;
  border:0 none;
  font-size:0;
  line-height: 0;
  text-indent:-9999px;
  border-radius: 8px;
  background:#f4f4f4 url('~@/assets/images/sp_index.png') no-repeat;
  background-position: 7px -193px;
  background-size: 1000px 1000px;
}
#contentBox #searchBox .searchInput > div > button:first-child {
  transition: background-position 0.2s ease;
}
#contentBox #searchBox.on .searchInput > div > button:first-child {
  background-position: -39px -193px;
}
#contentBox #searchBox .searchInput > div > input {
  border:0 none;
  border-radius: 8px;
  padding:0 10px;
  box-sizing: border-box;
  background:#f4f4f4;
}
#contentBox #searchBox .searchInput > div > input::placeholder {color:#333;}
#contentBox #searchBox .searchInput > div > input + button {
  background:#ff6600 url('~@/assets/images/sp_index.png') no-repeat;
  background-position: -94px -192px;
  background-size: 1000px 1000px;
}

#contentBox #searchBox .searchResult {
  overflow-y:scroll;
  position: fixed;
  top:100%;
  left:0;
  width:100%;
  height:calc(100% - 100px);
  padding:30px 18px;
  box-sizing: border-box;
  border-radius: 18px 18px 0 0;
  background: #fff;
  transition:top 0.5s cubic-bezier(0.22, 0.61, 0.36, 1);
}
#contentBox #searchBox.on .searchResult {
  top:50px;
}
#contentBox #popupDimmed {
  position: fixed;
  top:0;
  left:0;
  z-index: 900;
  width:100%;
  height: 100%;
  background: rgba(34, 34, 34, 0.5);
}
#contentBox #popupDimmed.on {
  display: block;
  opacity: 0;
  animation: aniDimmed 0.5s ease forwards;
}
.popupDimmed-enter,
.popupDimmed-leave-to {
  opacity: 0;
}
.popupDimmed-enter-active,
.popupDimmed-leave-active {
  transition: opacity 0.2s;
}
</style>
