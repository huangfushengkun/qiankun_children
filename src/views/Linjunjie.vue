<!--
 * @Description: 
 * @Version: 2.0
 * @Autor: huangfu
 * @Date: 2020-09-24 13:24:48
 * @LastEditors: huangfu
 * @LastEditTime: 2020-09-29 18:04:26
-->
<template>
  <div class="starbox">
    <div @click="onChangePage('/')">跳转到主应用</div>
    <div>林俊杰的铁粉 哈哈!!!!</div>
  </div>
</template>
<script>
export default {
  methods:{
    onChangePage(url){
      this.routerGo(url)
    },
    routerGo(href = '/', title = null, stateObj = {}) {
      window.history.pushState(stateObj, title, href); 
    },

  }
}
</script>

<style scoped  lang="scss" >
.starbox{
  div{
    text-align: center;
    font-size:20px;
    color:#8E2DE2;
    font-weight: 600;
    margin-bottom:20px;
  }
  img{
    width:400px;
    margin: 0 10px;
  }
}
</style>

