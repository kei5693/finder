<template>
  <div
    class="tabMenuBox"
    ref="tabMenuBox"
  >
    <!-- tabs -->
    <div
      class="tabs"
      ref="tabs"
    >
      <!-- tabitem -->
      <div 
        class="tabitem"
        v-for="(tab, index) in items"
        @click="switchTab(index)"
        :key="index"
        ref="tabitem"
      >
      {{tab}}
      </div>
      <!-- //tabitem -->
    </div>
    <!-- //tabs -->
  </div>
</template>
<script>

export default {
  data() {
    return {
      tabWidth: 0,
      items: ['Google', 'Microsoft', 'Samsung', 'Sony', 'LG', 'Google', 'Microsoft', 'Samsung', 'Sony', 'LG'],
    }
  },
  methods: {
    switchTab(n){
      var posCenter   = window.outerWidth / 2;
      var tabMenuBox  = this.$refs.tabMenuBox;
      var tabs        = this.$refs.tabs;
      var tabitem     = this.$refs.tabitem;
      var pos         = 0;
      var posLimit    = tabs.offsetWidth - tabMenuBox.offsetWidth;

      if( tabitem[n].offsetLeft + tabitem[n].offsetWidth / 2 <= posCenter ){
        //console.log('left');
        pos = 0;
      } else {
        //console.log('right');
        pos = (tabitem[n].offsetLeft + tabitem[n].offsetWidth / 2) - posCenter;
        if (pos > posLimit) {
          pos = posLimit
        }
      }
      
      function siblings(t) {
        var children = t.parentElement.children;
        var tempArr = [];

        for (var i = 0; i < children.length; i++) {
          tempArr.push(children[i]);
        }

        return tempArr.filter(function(e){
          return e != t;
        });
      }
      console.log(siblings(n));    



      tabMenuBox.scrollLeft = pos;
    },
    setTabInit(){
      for(var i in this.$refs.tabitem){
        this.tabWidth += this.$refs.tabitem[i].offsetWidth;
      }
      this.$refs.tabs.style.width = this.tabWidth+'px';
      this.$refs.tabitem[0].classList.add('on');
    }
  },
  mounted(){
    this.setTabInit();
  },
}
</script>
<style>
.tabMenuBox {
  overflow-x:scroll;
  overflow: -moz-scrollbars-none; 
  -ms-overflow-style: none; 
  scroll-behavior: smooth;
}
.tabMenuBox::-webkit-scrollbar  { 
  width: 0 !important;
  height:0 !important;
}
.tabs{
  display:flex;
  position:relative;
  background:#000;
  color:white;
  height:48px;
}
.tabitem{
  display:flex;
  align-items:center;
  justify-content:center;
  padding:0 20px;
  cursor:pointer;
  text-transform:uppercase;
  font-size:14px;
}
.tabitem.on {color:red;}
</style>