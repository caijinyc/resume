<template>
  <div class="career">
    <div class="career-wrapper">
      <div class="title">实习经历</div>
      <div class="text">
        <div class="company">
          <span class="company-title">{{ career.qunhe.name }}</span>
        </div>
        <p class="desc">{{ career.qunhe.desc }}</p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data () {
    return {
      career: {
        qunhe: {
          name: '酷家乐',
          position: '前端实习工程师',
          desc: ''
        }
      }
    }
  }
}
</script>

<style lang="scss">
@import "~common/scss/variable.scss";

.career {
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
  .career-wrapper {
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
      .company {
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
