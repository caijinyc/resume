<template>
  <div class="home">
    <div class="home-wrapper">
      <div class="avatar">
        <img src="./me3.jpg" width="170" height="170">
      </div>
      <div class="text">
        <p class="name">蔡锦 CaiJinyc</p>
        <p class="desc">一个热爱前端、充满热情、善于解决问题的前端工程师，希望找到能让我充分发挥这些特长的工作。</p>
        <p class="go">应聘岗位：前端开发实习生</p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
}
</script>

<style lang="scss" scoped>
@import "~common/scss/variable.scss";
@import "~common/scss/mixin.scss";
.home {
  position: fixed;
  top:0;
  left: 0;
  bottom: 0;
  right: 0;
  display: flex;
  align-items: center;
  justify-content: center;
  width: 100%;
  height: 100%;
  background: $color-background;
  .home-wrapper {
    width: 75%;
    text-align: center;
    .avatar {
      display: inline-block;
      width: 170px;
      height: 170px;
      // background: #fff;
      border-radius: 50%;
      // border: 10px solid rgba(255, 255, 255, 0.342);
      img {
        border-radius: 50%;
      }
    }
    .text {
      .name {
        padding: 30px 0;
        line-height: 45px;
        color: $color-text-title;
        font-size: 40px;
        font-weight: bold;
        letter-spacing: 1px;
      }
      .desc {
        font-size: $font-size-small;
        line-height: 23px;
        color: $color-text-l;
        @include justify1();
      }
      .go {
        font-size: $font-size-small-x;
        font-weight: bold;
        color: $color-text-title;
        padding: 20px 0 15px 0;
      }
    }
  }
}
</style>
