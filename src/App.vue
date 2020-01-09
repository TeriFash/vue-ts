<template>
  <div id="app">
    <div id="nav" class="nav">
      <router-link to="/">Home</router-link> |
      <router-link to="/about">About</router-link>
    </div>
    <transition :name="transitionName" mode="out-in">
      <router-view/>
    </transition>
  </div>
</template>

<script>
import MainComponent from '@/components/MainComponent.vue'

export default {
  data () {
    return {
      transitionName: 'fade'
    }
  }
}
</script>

<style lang="scss">
body {
  background-color: #393939;
}

#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: left;
  color: #fff;

  > div:not(.nav) {
    margin: 20px;
  }
}

#nav {
  padding: 30px;
  background-color: #2c2c2c;

  a {
    margin: 0 5px;
    font-weight: bold;
    color: #fff;

    &:first-child {
      margin-left: 0;
    }

    &:last-child {
      margin-right: 0;
    }

    &.router-link-exact-active {
      color: #42b983;
    }
  }
}

.fade-enter-active,
.fade-leave-active {
  transition-duration: 0.3s;
  transition-property: opacity;
  transition-timing-function: ease;
}

.fade-enter,
.fade-leave-active {
  opacity: 0
}
</style>
