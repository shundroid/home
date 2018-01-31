<template lang="pug">
  #app
    Header
    ProjectList
</template>

<script>
import Header from './components/Header.vue'
import ProjectList from './components/ProjectList.vue'

export default {
  name: 'app',
  components: {
    Header,
    ProjectList
  }
}
</script>

<style>
body {
  margin: 0;
}
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
}
.graphical-report__tooltip {
  user-select: none;
  pointer-events: none;
}
</style>
