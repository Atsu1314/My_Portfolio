<template>
  <div id="app">
    <Top :class="{welcome: get_in}" v-on:getIn="getIn()"></Top>
    <Main v-show="get_in" :class="{show: get_in}"></Main>
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
    }
  },
  methods: {
    getIn() {
      this.get_in = true
    }
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

.welcome{
  background: white!important;
  transition: all 600ms 0s ease;
}

.show{
  transition: all 600ms 0s ease;
}
</style>
