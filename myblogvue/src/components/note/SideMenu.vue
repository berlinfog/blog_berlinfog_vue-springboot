<template>
  <el-menu
    class="categories"
    default-active="0"
    @select="handleSelect"
    active-text-color="red">
    <el-menu-item index="/note">
      <i class="el-icon-menu"></i>
      <span slot="title">全部</span>
    </el-menu-item>
    <el-menu-item index="/diary">
      <i class="el-icon-menu"></i>
      <span slot="title">日记</span>
    </el-menu-item>
    <el-menu-item index="/write">
      <i class="el-icon-menu"></i>
      <span slot="title">笔记</span>
    </el-menu-item>
    <el-menu-item index="/noteother">
      <i class="el-icon-menu"></i>
      <span slot="title">其他</span>
    </el-menu-item>
  </el-menu>
</template>

<script>
  export default {
    name: 'SideMenu'
  }
</script>

<style scoped>
  .categories {
    position: fixed;
    margin-left: 50%;
    left: -850px;
    top: 100px;
    width: 150px;
  }
</style>

