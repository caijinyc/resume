<template>
  <div class="home">
    <div class="home-wrapper">
      <div class="avatar">
        <!-- <img src="" width="150" height="150"> -->
      </div>
      <div class="text">
        <p class="name">蔡锦 CaiJinyc</p>
        <p class="desc">一个热爱前端、会点设计、善于解决问题的前端工程师。快招我到碗里来吧~</p>
        <p class="go">应聘岗位：前端开发实习生</p>
        <p class="contact">
          <a class="email" href="mailto:me@caijin.tech">me@caijin.tech</a>
          <span class="tel">tel: 15344315015</span>
        </p>
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
      border: 10px solid rgba(255, 255, 255, 0.342)
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
        font-size: 16px;
        line-height: 23px;
        color: $color-text-l;
        @include justify1();
      }
      .go {
        font-size: 18px;
        font-weight: bold;
        color: $color-text-title;
        padding: 20px 0 15px 0;
      }
      .contact {
        font-size: 18px;
        .email {
          padding-right: 10px;
          color: $color-text-title;
          &:hover {
            color: aqua;
            transition: all 1s;
          }
        }
        .tel {
          color: $color-text-title;
        }
      }
    }
  }
}
</style>
