<template>
  <div id="app">
  <page-tweet></page-tweet>
  </div>
</template>

<script>
import PageTweet from './components/tweets.vue'

export default {
  name: 'App',
  components: {
    PageTweet
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
