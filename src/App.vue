<template>
  <div id="app">
    <BlogHome />
  </div>
</template>

<script>
import BlogHome from './components/BlogHome.vue'

export default {
  name: 'app',
  components: {
    BlogHome
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
