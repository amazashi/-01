<script setup>
import HelloWorld from './components/HelloWorld.vue'
import TopMenu from "./components/TopMenu.vue";
import Siderbar from "./components/Siderbar.vue";
</script>

<!--</style>-->
<template>
  <div id="app">
    <!-- 顶部菜单栏 -->
    <TopMenu />

    <div class="main-content">
      <!-- 左侧侧边栏 -->
<!--      <div class="sidebar">-->
<!--        <ul>-->
<!--          <li @click="changePage('home')">首页</li>-->
<!--          <li @click="changePage('about')">关于</li>-->
<!--          <li @click="changePage('contact')">联系我们</li>-->
<!--        </ul>-->
<!--      </div>-->
      <Siderbar @changePage="changePage" />

      <!-- 右侧展示区域 -->
      <div class="page-content">
        <component :is="currentPageComponent"></component>
      </div>
    </div>
  </div>
</template>

<script>
import HomePage from './views/HomePage.vue'
import AboutPage from './views/AboutPage.vue'
import ContactPage from './views/ContactPage.vue'

export default {
  name: 'App',
  data() {
    return {
      currentPage: 'home', // 默认页面
    };
  },
  computed: {
    currentPageComponent() {
      // 根据当前选中的页面渲染不同的组件
      if (this.currentPage === 'home') {
        return HomePage;
      } else if (this.currentPage === 'about') {
        return AboutPage;
      } else if (this.currentPage === 'contact') {
        return ContactPage;
      }
    }
  },
  methods: {
    changePage(page) {
      this.currentPage = page;
    }
  }
};
</script>

<style scoped>
#app {
  display: flex;
  flex-direction: column;
  height: 100vh;
}

.top-menu {
  background-color: #333;
  color: white;
  height: 2vh; /* 设置顶部菜单栏的高度为 3vh */
  display: flex;
  justify-content: center;
  align-items: center; /* 垂直居中 */
}
.menu {
  display: flex;
  //justify-content: space-evenly; /* 使菜单项均匀分布 */
  list-style-type: none;
  margin: 0;
  padding: 0;
  width: 100%;
}

.menu li {
  cursor: pointer;
  padding: 0 20px;
  transition: background-color 0.3s ease;
}

.menu li:hover {
  background-color: #575757; /* 设置鼠标悬停时的背景色 */
}

.main-content {
  display: flex;
  height: calc(100vh - 3vh); /* 去掉顶部菜单栏的高度 */
}

.main-content {
  display: flex;
  height: calc(100vh - 2vh); /* 去掉顶部菜单栏的高度 */
}

.sidebar {
  width: 250px;
  background-color: #4a76c9;
  padding: 20px;
  box-sizing: border-box;
}

.sidebar ul {
  list-style-type: none;
  padding: 0;
}

.sidebar li {
  cursor: pointer;
  padding: 10px 0;
}

.sidebar li:hover {
  background-color: #ddd;
}

.page-content {
  flex: 1;
  padding: 20px;
  background-color: #fff;
  box-sizing: border-box;
  overflow-y: auto;
  color: black;
}
</style>
