<template>
  <div id="app" @mousewheel="changePage">
    <transition name="home">
      <div class="home-wrapper" v-show="page === 0">
        <home></home>
      </div>
    </transition>
    <transition name="projects">
      <div class="projects-wrapper" v-show="page === 1">
        <projects></projects>
      </div>
    </transition>
    <transition name="projects">
      <div class="projects-wrapper" v-show="page === 2">
        <professions></professions>
      </div>
    </transition>
  </div>
</template>

<script>
import Home from './components/home/home'
import Projects from 'components/projects/projects'
import Professions from 'components/professions/professions'

export default {
  data () {
    return {
      page: 0
    }
  },
  methods: {
    changePage (item) {
      console.log(item.wheelDelta)
      let x = item.wheelDelta
      if (x < 0) {
        this.page++
      } else if (this.page > 0) {
        this.page--
      }
    }
  },
  components: {
    Home,
    Projects,
    Professions
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
  .home-wrapper {
    &.home-enter-active, &.home-leave-active {
      transition: all 0.2s;
    }
    &.home-enter, &.home-leave-to {
      opacity: 0;
    }
  }
  .projects-wrapper {
    &.projects-enter-active, &.projects-leave-active {
      transition: all 0.2s;
    }
    &.projects-enter, &.projects-leave-to {
      opacity: 0;
    }
  }
}
</style>
