<!-- src/components/TopMenu.vue -->
<template>
  <div class="top-menu">
    <ul class="menu">
      <li>文件</li>
      <li>编辑</li>
      <li>段落</li>
      <li>格式</li>
      <li>视图</li>
      <li>主题</li>
      <li>帮助</li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'TopMenu'
};
</script>

<style scoped>
.top-menu {
  background-color: #333;
  color: white;
  height: 3.5vh; /* 设置顶部菜单栏的高度为 3vh */
  display: flex;
  align-items: center; /* 垂直居中菜单项 */
}

.menu {
  display: flex;
  list-style-type: none;
  margin: 0;
  padding: 0;
  width: 100%; /* 使菜单项占满整个宽度 */
}

.menu li {
  cursor: pointer;
  width: 3.3vw; /* 每个菜单项占用 5vw 宽度 */
  text-align: center; /* 文字居中 */
  line-height: 3.5vh; /* 设置行高与菜单栏高度相同，确保文字垂直居中 */
  padding: 0.5vh 0; /* 为上下添加 0.5vh 的内边距 */
  margin: 2px;
  transition: background-color 0.3s ease;
}

.menu li:hover {
  background-color: #575757; /* 悬停时背景色变化 */
}
</style>
