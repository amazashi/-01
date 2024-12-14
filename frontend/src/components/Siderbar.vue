<script setup>

</script>
<template>
  <div class="sidebar">
    <ul>
      <li @click="changePage('home')">首页</li>
      <li @click="changePage('about')">关于</li>
      <li @click="changePage('contact')">联系我们</li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'Sidebar',
  methods: {
    // 用来通知父组件切换页面
    changePage(page) {
      this.$emit('changePage', page);
    }
  }
};
</script>

<style scoped>
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
</style>