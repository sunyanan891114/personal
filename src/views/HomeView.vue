<template>
  <el-header><NavigationBar></NavigationBar></el-header>
  <el-main>
    <el-row class="ep-bg-purple">
      <div class="decorator decorator-y">
        <img src="../assets/images/Y.png" alt="Y" />
      </div>
      <div class="decorator decorator-n">
        <img src="../assets/images/N.png" alt="N" />
      </div>
      <div class="decorator decorator-s">
        <img src="../assets/images/S.png" alt="S" />
      </div>
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
      <el-col :span="12">
        <div class="grid-content photo">
          <img src="../assets/images/man-01-458x744.png" height="744" width="458" />
        </div>
      </el-col>
    </el-row>
  </el-main>
  <section class="section"></section>
</template>

<script lang="ts" setup>
import NavigationBar from '@/components/NavigationBar.vue'
</script>

<style scoped lang="scss">
.box-retro-content {
  padding-top: 210px;
  padding-bottom: 210px;
}

.title,
.introduction {
  width: 500px;
  margin: auto 0 auto auto;
}

.title {
  font-size: $font-size-title;
  line-height: 1;
  position: relative;

  &:before {
    content: '';
    display: block;
    position: absolute;
    top: 30px;
    left: -35px;
    width: 30px;
    height: 4px;
    background-color: $color-primary;
  }
}

.introduction {
  color: $font-color-secondary;
  margin-top: 30px;
  width: 521px;
  line-height: 1.5;
}

.photo {
  position: relative;
  height: 744px;

  &:before {
    z-index: -1;
    content: '';
    position: absolute;
    top: -100vh;
    bottom: 0;
    left: 100px;
    right: 0;
    background-color: $color-primary;
    pointer-events: none;
    width: 500px;
  }
}

.decorator {
  position: absolute;
  animation-name: fadeIn;
  animation-duration: 1s;

  &-y {
    right: calc(50% + 500px + 35px);
    top: 4%;
    transform: translate3d(0px, 0.029px, 0px) rotateX(0deg) rotateY(0deg) rotateZ(0deg) scaleX(1)
      scaleY(1) scaleZ(1);
  }

  &-n {
    bottom: 7%;
    right: calc(50% + 500px + 185px);
  }

  &-s {
    bottom: 19%;
    left: calc(50% + 500px + 160px);
  }
}
</style>
