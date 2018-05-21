<template>
  <div class="projects">
    <div class="projects-wrapper">
      <div class="title">项目经验</div>
      <div class="vue-music">
        <div class="img">
          <img src="./music.svg" alt="">
        </div>
        <p class="name" >
          <span @click="linkGithubMusic">Vue 网易云音乐 WebApp</span>
        </p>
        <p class="desc">一款移动端音乐 WebApp，使用了 Vue、vue-router、vuex、axios、ES6 语法、SCSS 等开发。UI 界面参考了安卓版的网易云音乐、flex 布局适配常见移动端，实现了搜索、本地收藏、歌词、播放列表、播放模式（循环播放、随机播放、顺序播放）等功能，在 Github 上获得了 750+ star。</p>
      </div>
      <div class="vue-music">
        <p class="name" >
          <span @click="linkGithubGame">扫雷游戏</span>
        </p>
        <p class="desc">使用原生 JavaScript 实现的一个扫雷游戏，实现了扫雷游戏的基本功能，例如：计时、选择游戏难度、随机生成地雷地图、标记地雷、剩余地雷、自动连锁点开、游戏成功和失败的动画等功能。</p>
      </div>

    </div>
  </div>
</template>

<script>
export default {
  methods: {
    linkGithubMusic () {
      window.open('https://github.com/CaiJinyc/vue-music-webapp')
    },
    linkGithubGame () {
      window.open('https://github.com/CaiJinyc/game-mineSweepinng')
    }
  }
}
</script>

<style lang="scss">
@import "~common/scss/variable.scss";

.projects {
  position: fixed;
  display: flex;
  align-items: center;
  justify-content: center;
  top:0;
  left: 0;
  bottom: 0;
  right: 0;
  width: 100%;
  height: 100%;
  background: $color-background;
  .projects-wrapper {
    width: 80%;
    margin-bottom: 50px;
    text-align: center;
    .title {
      padding: 20px 0;
      color: $color-text-title;
      font-size: 40px;
      font-weight: bold;
      letter-spacing: 1px;
    }
    .vue-music {
      margin-top: 20px;
      img {
        width: 80px;
        height: 80px;
        opacity: 0.8;
      }
      .name {
        margin: 15px 0 10px 0;
        font-size: $font-size-medium-x;
        color: $color-text-title;
        transition: all 1s;
        span {
         font-weight: bold;
          transition: all 1s;
          &:hover {
            cursor: pointer;
            color: aqua;
          }
        }
      }
      .desc {
        display: inline-block;
        max-width: 800px;
        font-size: 16px;
        line-height: 23px;
        color: $color-text-l;
      }
    }
  }
}
</style>
