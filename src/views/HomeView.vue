<template>
  <el-header><NavigationBar></NavigationBar></el-header>
  <el-main>
    <el-row class="ep-bg-purple">
      <el-col :span="12">
        <div class="grid-content box-retro-content">
          <h1 class="title">
            I'm Yanan Sun. <br />
            UI Developer
          </h1>
          <p class="introduction">
            I am a web developer focused on crafting great web experiences. I enjoy creating
            beautifully designed, intuitive and functional websites for my clients.
          </p>
        </div>
      </el-col>
      <el-col :span="12"><div class="grid-content photo" /></el-col>
    </el-row>
  </el-main>
  <section class="section"></section>
</template>

<script lang="ts" setup>
import NavigationBar from '@/components/NavigationBar.vue'
</script>

<style>
.box-retro-content {
  padding-top: 210px;
  padding-bottom: 210px;
}
</style>
