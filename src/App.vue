<template lang="pug">
#app
  Header
  Profile
  ProjectList
</template>

<script lang="ts">
import { defineComponent } from 'vue'
import Header from './components/Header.vue'
import Profile from './components/Profile.vue'
import ProjectList from './components/ProjectList.vue'

export default defineComponent({
  name: 'App',
  components: {
    Header,
    Profile,
    ProjectList
  }
})
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
a {
  color: black;
}
</style>
