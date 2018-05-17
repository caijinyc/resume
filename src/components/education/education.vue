<template>
  <div class="projects">
    <div class="projects-wrapper">
      <div class="title">教育背景</div>
      <div class="text">
        <div class="edu">
          <span class="school">{{education.school}}</span>
        </div>
        <p class="major">{{education.major}}</p>
        <p class="graduation">{{education.graduation}}</p>
        <p class="desc">{{education.desc}}</p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data () {
    return {
      education: {
        school: '吉林建筑大学',
        major: '视觉传达专业',
        graduation: '2015.9 - 2019.6'
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
        padding: 20px 0;
        color: $color-text-title;
        font-size: 40px;
        font-weight: bold;
        letter-spacing: 1px;
    }
    .text {
      .edu {
        margin: 20px 0 20px 0;
        color: $color-text-title;
        font-size: 25px;
        span {
          font-weight: bold;
        }
      }
      .major, .graduation  {
        margin: 5px 0;
        line-height: 23px;
        font-size: 16px;
        color: $color-text-l;
      }
    }
  }
}
</style>
