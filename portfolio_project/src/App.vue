<template>
  <div id="app">
    <Header></Header>
    <Top></Top>
    <!-- <HelloWorld msg="Welcome to Your Vue.js App"/> -->
  </div>
</template>

<script>
// import HelloWorld from './components/HelloWorld.vue'
import Header from './components/parts/Header.vue'
import Top from './components/parts/Top.vue'


export default {
  name: 'App',
  components: {
    // HelloWorld,
    Header,
    Top,
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
  margin-top: 20px;
}
</style>
