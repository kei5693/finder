<template>
  <div id="contentBox">
    <div id="header">
      <img src="" alt="Finder">
      <div>
        <button type="button">오늘</button>
        <button type="button">Salesgram</button>
      </div>
    </div>
    <div id="searchBox">
      <div class="searchInput">
        <div>
          <button type="button"></button>
          <input type="text" placeholder="찾으시는 태그를 입력해주세요." />
          <button type="button"></button>
        </div>
      </div>
      <div class="searchResult">
          
      </div>
    </div>
  </div>
</template>

<script>

export default {
  name: 'Home',
  components: {
    
  }
}
</script>

<style>
html, body, #app, #contentBox {height:100%;}
#contentBox {
  background: #EBF0F3;
}

#searchBox {
  position: absolute;
  bottom:0;
  left:0;
  width:100%;
  background: tomato;
}
</style>
