<!-- 页面 -->
<template>
  <div>
    <div class="topNav">
      <div class='logo'>LOGO</div>
      <ul class='menu'>
        <li>菜单1</li>
        <li>菜单2</li>
      </ul>
      <i class="iconfont toggleAside" @click="toggleMenu">&#xe604;</i>
    </div>
  </div>
</template>
<script>
import { inject } from 'vue'

export default {
  name: "TopNav",
  setup() {
    const menuVisible = inject('menuVisible')
    console.log(menuVisible.value);
    const toggleMenu = () => {
      menuVisible.value = !menuVisible.value
    }
    return { toggleMenu }
  },
  mounted() {

  },
  data() {
    return {};
  },
  methods: {}
};
</script>
<style scoped>
.topNav{
  background: pink;
  display: flex;
  height: 50px;
  position: relative;
  z-index: 10;
  justify-content: center;
  align-items: center;
}

.toggleAside{
  line-height: 24px;
  width: 24px;
  height: 24px;
  position: absolute;
  left: 16px;
  top: 50%;
  transform: translateY(-50%);
  display: none;
}

.logo{
  text-align: center;
  max-width: 6em;
  margin-right: auto;
  margin-left: 1em;
  line-height: 50px;
  font-weight: 600;
}

.menu{
  display: flex;
  white-space: nowrap;
  flex-wrap: nowrap;
  line-height: 50px;
  font-weight: 600;
}

li{
  list-style: none;
  margin: 0 1em;
}

@media (max-width: 500px){
  .menu{
    display: none;
  }

  .logo{
    margin: 0 auto;
  }

  .toggleAside{
    display: inline-block;
  }
}

</style>
