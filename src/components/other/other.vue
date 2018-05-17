<template>
  <div class="projects">
    <div class="projects-wrapper">
      <div class="title">了解更多</div>
      <div class="text">
          <div class="more">
              <span class="home">个人主页</span>
              <span class="github">Github</span>
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
        graduation: '2019年届毕业生'
      }
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
          font-weight: bold;  
        }
      }
      .edu {
        margin: 20px 0 10px 0;
        color: $color-text-title;
        font-size: 25px;
        span {
          font-weight: bold;
        }
      }
      .major, .graduation  {
        margin: 10px 0;
        line-height: 23px;
        font-size: 16px;
        color: $color-text-l;
      }
    }
  }
}
</style>
