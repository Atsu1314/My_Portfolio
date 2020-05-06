<template>
  <div id="app">
    <Top v-show="!delete_top" :class="{welcome: get_in}" v-on:getIn="getIn()"></Top>
    <Main v-show="delete_top" :class="{show: get_in}" :showMain="get_in"></Main>
    <Footer/>
  </div>
</template>

<script>
import Footer from './components/parts/Footer.vue'
import Top from './views/Top.vue'
import Main from './views/Main.vue'

export default {
  name: 'App',
  components: {
    Top,
    Main,
    Footer,
  },
  data(){
    return{
      get_in: false,
      delete_top: false,
    }
  },
  methods: {
    getIn() {
      this.get_in = true
      setTimeout(() => this.delete_top = true,600)
    },
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
}

.welcome{
  background-color:#ffc978;
  opacity: 0.5;
  transition: all 500ms 0ms ease;
}
</style>
