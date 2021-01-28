<!-- 页面 -->
<template>
  <div>
    <TopNav/>
    <div class='content'>
      <aside class="componentList" v-if="menuVisible">
        <h2>组件列表</h2>
        <ol>
          <li>
            <Router-link to="/doc/switch">Switch 组件</Router-link>
          </li>

          <li>
            <Router-link to="/doc/button">button 组件</Router-link>
          </li>
          <li>
            <Router-link to="/doc/dialog">Dialog 组件</Router-link>
          </li>
          <li>
            <Router-link to="/doc/tabs">Tabs 组件</Router-link>
          </li>

        </ol>
      </aside>
      <main>
        <router-view></router-view>
      </main>
    </div>
  </div>
</template>
<script>
import TopNav from "../components/TopNav.vue";
import { inject } from "vue";

export default {
  name: "Doc",
  setup(){
    const menuVisible =inject('menuVisible')
    return {menuVisible}

  },
  mounted() {

  },
  data() {
    return {};
  },
  methods: {},
  components: { TopNav }
};
</script>
<style lang='css' scoped>
aside{
  background: lightblue;
  width: 150px;
  padding: 70px 16px 16px 16px;
  position: fixed;
  top: 0;
  left: 0;
}

aside h2{
  margin-bottom: 4px;
  text-align: left;
}

aside ol li{
  list-style: none;
  padding: 4px 0;
  text-align: left;

}

a{
  color: black;
  font-weight: 600;
  text-decoration: none;
  text-align: left;

}
</style>
