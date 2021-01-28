<!-- 页面 -->
<template>
  <div class='content'>
    <TopNav/>
    <div class='banner'>
      <h1>wwj-UI</h1>
      <h2>一个厉害的UI框架</h2>
      <p class='actions'>
        <a href='https://www.yuque.com/dashboard/my_books' class="goGit">GitHub</a>
        <Router-link to='/doc' class="goDoc">开始</Router-link>
      </p>
    </div>
  </div>
</template>
<script lang='ts'>
import TopNav from "../components/TopNav.vue";
export default {
  name: "Home",
  mounted() {

  },
  data() {
    return {};
  },
  methods: {},
  components:{TopNav}
};
</script>
<style lang='css' scoped>
.content{
  width: 100%;
  height: 100%;
  box-sizing: border-box;
  position: relative;
}
.banner{
  width: 100%;
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;
  background: aqua;
  position: absolute;
  top: 50px;
  bottom: 0;
  left: 0;
}
.actions{
  margin-top: 10px;
}
.goGit,.goDoc{
  background: azure;
  border-radius: 10px;
  padding: 3px;
  text-decoration: none;
  color: black;
  margin-right:10px;
}

</style>
