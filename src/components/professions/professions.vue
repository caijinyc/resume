<template>
  <div class="projects">
    <div class="projects-wrapper">
      <div class="title">掌握技能</div>
      <div class="text">
        <div class="htmlcss">
          <h1 class="name">HTML/CSS</h1>
          <p>{{professions.htmlcss}}</p>
          <p>{{professions.scss}}</p>
        </div>
        <div class="javascript">
          <h1 class="name">JavaScript</h1>
          <p>{{professions.js}}</p>
          <p>{{professions.vue}}</p>
        </div>
        <div class="other">
          <h1 class="name">其他</h1>
          <p>{{professions.other}}</p>
          <p>{{professions.design}}</p>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data () {
    return {
      professions: {
        htmlcss: '熟练使用 HTML5、CSS3，能够编写语义化的 HTML，模块化的 CSS，能够完成比较复杂的布局。',
        scss: '熟练使用 SCSS、Autoprefixer、Bootstrap 等 CSS 预处理和框架。',
        js: '熟练使用 原生 JavaScript、ES6、AJAX 能够运用模块化的方式编程。',
        vue: '熟练使用 Vue.js、vuex、vue-router 等工具开发项目。',
        other: '熟悉 Webpack 等前端自动化工具，熟悉 Git 版本管理工具。',
        design: '熟练使用 Photoshop、Illustrator 等设计工具，有一定的审美能力，能够准确还原设计稿。'
      }
    }
  },
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
        padding: 20px 0;
        color: $color-text-title;
        font-size: 40px;
        font-weight: bold;
        letter-spacing: 1px;
    }
    .text {
      .name {
        margin: 20px 0;
        color: $color-text-title;
        font-size: $font-size-medium-x;
        font-weight: bold;
      }
      p {
        font-size: $font-size-small;
        line-height: 23px;
        color: $color-text-l;
      }
    }
  }
}
</style>
