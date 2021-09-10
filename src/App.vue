<template>
  <div id="app">
    <tool-bar @trigger-popover="openPopover"/>
    <icon-bar />
    <component v-show="togglePopover" :is="popoverType" @close-popover="closePopover" />
  </div>
</template>

<script>
import ApplePopover from './components/ApplePopover';
import IconBar from './components/IconBar';
import ToolBar from './components/ToolBar';

export default {
  name: 'App',
  components: {
    ToolBar,
    ApplePopover,
    IconBar
  },
  data() {
    return {
      popoverType: false,
      togglePopover: false
    }
  },
  methods: {
    openPopover(type) {
      this.togglePopover = true;
      this.popoverType = type;
    },
    closePopover() {
      this.togglePopover = false;
    }
  }
}
</script>

<style lang="scss">
html {
  background: url('~@/assets/macos-big-sur.jpg') no-repeat center center fixed;
  background-size: cover;
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

</style>
