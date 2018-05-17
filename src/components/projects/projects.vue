<template>
  <div class="projects">
    <div class="projects-wrapper">
      <div class="title">项目经验</div>
      <div class="vue-music">
        <div class="img">
          <img src="./music.svg" alt="">
        </div>
        <p class="name" >
          <span @click="linkGithub">Vue 网易云音乐 WebApp</span>
        </p>
        <p class="desc">基于 Vue(2.5) + vuex + vue-router + vue-axios +better-scroll + Scss + ES6 等开发一款移动端音乐 WebApp，UI 界面精美、flex 布局适配常见移动端。</p>
      </div>

    </div>
  </div>
</template>

<script>
export default {
  methods: {
    linkGithub () {
      window.open('https://github.com/CaiJinyc/vue-music-webapp')
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
        padding: 30px 0;
        color: $color-text-title;
        font-size: 40px;
        font-weight: bold;
        letter-spacing: 1px;
    }
    .vue-music {
      img {
        width: 80px;
        height: 80px;
        opacity: 0.8;
      }
      .name {
        margin: 15px 0 10px 0;
        font-size: 25px;
        color: $color-text-name;
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
        max-width: 600px;
        font-size: 16px;
        line-height: 23px;
        color: $color-text-l;
      }
    }
  }
}
</style>
