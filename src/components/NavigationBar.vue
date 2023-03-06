<template>
  <el-menu
    :default-active="activeIndex"
    class="menu"
    mode="horizontal"
    :ellipsis="false"
    @select="handleSelect"
  >
    <el-menu-item index="0">Yanan Sun</el-menu-item>
    <div class="flex-grow" />
    <el-menu-item index="1">Home</el-menu-item>
    <el-menu-item index="2">Blogs</el-menu-item>
    <el-menu-item index="3">Contact Me</el-menu-item>
  </el-menu>
</template>

<script lang="ts" setup>
import { ref } from 'vue'

const activeIndex = ref('1')
const handleSelect = (key: string, keyPath: string[]) => {
  console.log(key, keyPath)
}
</script>

<style>
.menu.el-menu {
  position: sticky;
  z-index: 1;
  background: none;
}

.flex-grow {
  flex-grow: 1;
}
</style>
