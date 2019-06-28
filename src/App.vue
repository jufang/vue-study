<template>
  <div id="app">
    <!-- <HelloWorld msg="Welcome to Your Vue.js App"/> -->
    <Communicate/>
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import Communicate from './components/communicate';

export default {
  name: 'app',
  components: {
    HelloWorld,
    Communicate
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
