<template>
  <Navbar />
  <Welcome />
  <Intro />
  <Video />
</template>

<script>
import Navbar from './components/Navbar.vue'
import Welcome from './components/Welcome.vue'
import Intro from './components/Intro.vue'
import Video from './components/Video.vue'

export default {
  name: 'App',
  components: { Navbar, Welcome, Intro, Video }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}
</style>
