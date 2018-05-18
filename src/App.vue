<template>
  <div id="app" @mousewheel="changePage"
  @touchstart="touchstart"
  @touchend="touchend"
  >
    <transition name="trs">
      <div class="home-wrapper" v-show="page === 0">
        <home></home>
      </div>
    </transition>
    <transition name="trs">
      <div class="projects-wrapper" v-show="page === 1">
        <projects></projects>
      </div>
    </transition>
    <transition name="trs">
      <div class="projects-wrapper" v-show="page === 2">
        <professions></professions>
      </div>
    </transition>
    <transition name="trs">
      <div class="education-wrapper" v-show="page === 3">
        <education></education>
      </div>
    </transition>
    <transition name="trs">
      <div class="other-wrapper" v-show="page === 4">
        <other></other>
      </div>
    </transition>
    <div class="dots">
      <ul>
        <li v-for="(item, index) in pages" :key="item" :class="{'active': index === page}" @click="toPage(index)">
          <span class="text">{{item}}</span>
        </li>
      </ul>
    </div>
  </div>
</template>

<script>
import Home from './components/home/home'
import Projects from 'components/projects/projects'
import Professions from 'components/professions/professions'
import Education from 'components/education/education'
import Other from 'components/other/other'

export default {
  data () {
    return {
      page: 0,
      pages: ['首页', '项目', '技能', '教育', '联系']
    }
  },
  created () {
    this.canChange = true
  },
  mounted () {
    document.addEventListener('keydown', (item) => {
      // console.log(item.keyCode)
      if ((item.keyCode === 38 || item.keyCode === 37) && this.page > 0) {
        this.page--
      }
      if ((item.keyCode === 39 || item.keyCode === 40) && this.page < this.pages.length - 1) {
        this.page++
      }
    })
  },
  methods: {
    touchstart (item) {
      this.touchStartY = item.changedTouches[0].pageY
    },
    touchend (item) {
      let touchendY = item.changedTouches[0].pageY
      let diff = this.touchStartY - touchendY
      if (diff > 50 && this.page < this.pages.length - 1) {
        this.page++
      } else if (diff < -50 && this.page > 0) {
        this.page--
      }
    },
    changePage (item) {
      if (!this.canChange) {
        return
      }
      this.canChange = false
      setTimeout(() => {
        this.canChange = true
      }, 300)
      // console.log(item.wheelDelta)
      let x = item.wheelDelta
      if (x < 0 && this.page < this.pages.length - 1) {
        this.page++
      } else if (x > 0 && this.page > 0) {
        this.page--
      }
    },
    toPage (index) {
      this.page = index
    }
  },
  components: {
    Home,
    Projects,
    Professions,
    Education,
    Other
  }
}
</script>

<style lang="scss" scope>
@import "./common/scss/reset.scss";
@import "./common/scss/variable.scss";

#app {
  position: fixed;
  top:0;
  left: 0;
  bottom: 0;
  right: 0;
  width: 100%;
  height: 100%;
  background: $color-background;
  .trs-enter-active, .trs-leave-active {
    transition: all 0.2s;
  }
  .trs-enter, .trs-leave-to {
    opacity: 0;
  }
  .dots {
    position: fixed;
    @media only screen and (max-width: 600px) {
      left: 50%;
      bottom: 2%;
      transform: translateX(-50%);
      ul {
        li {
          display: inline-block;
          margin: 0 3px;
        }
      }
    }
    @media only screen and (min-width: 600px) {
      left: 3%;
      top: 50%;
      transform: translateY(-50%);
      ul {
        li {
        margin: 10px 0;
        &:hover {
          background: rgba(255, 255, 255, .9);
          .text {
            opacity: 1;
          }
        }
        }
      }
    }
    ul {
      li {
        position: relative;
        width: 10px;
        height: 10px;
        background: rgba(255, 255, 255, .5);
        transition: all 0.3s;
        border-radius: 50%;
        cursor: pointer;
        &.active {
          background: rgba(255, 255, 255, .9);
        }
        .text {
          position: absolute;
          left: 15px;
          top: -2px;
          width: 50px;
          color: $color-text-l;
          opacity: 0;
          font-size: 14px;
          transition: all 0.3s;
        }
      }
    }
  }
}
</style>
