<template>
  <Navbar />
  <Welcome />
  <Intro />
  <Video />
  <Facts />
</template>

<script>
import Navbar from './components/Navbar.vue'
import Welcome from './components/Welcome.vue'
import Intro from './components/Intro.vue'
import Video from './components/Video.vue'
import Facts from './components/Facts.vue'

export default {
  name: 'App',
  components: { Navbar, Welcome, Intro, Video, Facts }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}
</style>
