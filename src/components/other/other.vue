<template>
  <div class="projects">
    <div class="projects-wrapper">
      <div class="title">了解更多</div>
      <div class="text">
          <div class="more">
              <span class="home" @click="goBlog">个人主页</span>
              <span class="github" @click="goGithub">Github</span>
          </div>
          <p class="email"><span class="tit">Email: </span>{{other.email}}</p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data () {
    return {
      other: {
        email: 'me@caijin.tech',
        major: '视觉传达专业',
        graduation: '2019年届毕业生',
        blog: 'http://caijin.tech/blog/',
        github: 'https://github.com/CaiJinyc'
      }
    }
  },
  methods: {
    goBlog () {
      window.open(this.other.blog)
    },
    goGithub () {
      window.open(this.other.github)
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
    .text {
      .more {
        margin: 20px 0 10px 0;
        color: $color-text-title;
        font-size: 25px;
        span {
          cursor: pointer;
          font-weight: bold;
          transition: all 1s;
          &:hover {
            color: $color-text-highlight;
          }
        }
      }
    }
  }
}
</style>
