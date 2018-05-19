<template>
  <div class="projects">
    <div class="projects-wrapper">
      <div class="title">了解更多</div>
      <div class="text">
          <div class="more">
              <span class="home" @click="goBlog">个人主页</span>
              <span class="more-divide"></span>
              <span class="github" @click="goGithub">Github</span>
          </div>
          <div class="contact">
            <h1 class="contact-title">如果觉得我还不错的话，招我招我招我吧</h1>
            <p class="tel"><span class="tit">Tel: </span>{{other.tel}}</p>
            <p class="email"><span class="tit">Email: </span>
              <a href="mailto:me@caijin.tech">{{other.email}}</a>
            </p>
          </div>
          <div class="download"><span>下载简历</span></div>
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
        tel: '153-4431-5015',
        qq: '610304098',
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
        padding: 20px 0;
        color: $color-text-title;
        font-size: 40px;
        font-weight: bold;
        letter-spacing: 1px;
    }
    .text {
      .more {
        margin: 20px 0 20px 0;
        color: $color-text-name;
        font-size: $font-size-medium-x;
        .more-divide {
          display: inline-block;
          position: relative;
          top: 3px;
          width: 7px;
          height: 26px;
          background: $color-text-title;
        }
        span {
          margin: 0 5px;
          cursor: pointer;
          font-weight: bold;
          transition: all 1s;
          &:hover {
            color: $color-text-highlight;
          }
        }
      }
      .contact {
        p {
          display: inline-block;
          margin: 0 10px;
        }
        .contact-title {
          padding: 10px 0;
          line-height: 30px;
          color: $color-text-title;
          font-weight: bold;
          font-size: $font-size-medium-x;
        }
          .email {
            font-size: 0;
            .tit, a {
              font-size: $font-size-small;
            }
            a {
              color: $color-text-l;
              transition: all 1s;
              &:hover {
                color: $color-text-highlight;
              }
            }
          }
      }
      .download {
        margin: 10px;
        font-size: $font-size-medium-x;
        color: rgb(0, 255, 255);
        span {
          font-weight: bold;
          transition: all 1s;
          cursor: pointer;
          &:hover {
            color: $color-text-name;
          }
        }
      }
    }
  }
}
</style>
