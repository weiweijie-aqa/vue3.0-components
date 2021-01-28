<template>
  <router-view class="routerView"></router-view>
</template>

<script>
import {ref,provide} from 'vue'
import { router } from "./router";

export default {
  name: 'App',
  setup(){
    const width=document.documentElement.clientWidth;

    let menuVisible=ref(width > 500);
    provide('menuVisible',menuVisible)
    router.afterEach(()=>{
      console.log("我执行了111");
      if(width<=500){
        menuVisible.value=false
      }
    })
  }
}




</script>
<style lang=css scoped>
.routerView{
  width: 100%;
  height: 100%;
  box-sizing: border-box;
}
</style>
