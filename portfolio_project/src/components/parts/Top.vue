<template id="">
  <div class="jumbotron junbotron-extend" :class="{welcome : get_in}">
    <div class="container-fluid text-center">
      Wlcome to <p class="name">Muta Atsuyoshi's</p> Portfolio!
    </div>
    <div class="btn" @click='welcome' :class="{clicked : get_in}"><p>Get in</p></div>
  </div>
</template>

<script type="text/javascript">
  export default {
    data() {
      return {
      get_in : false,
      }
    },
    methods: {
      welcome() {
        this.get_in = !this.get_in
      }
    }
  }
</script>

<style media="screen" scoped>
@import url('https://fonts.googleapis.com/css?family=Sawarabi+Mincho');
.junbotron-extend{
  position:relative;
  height: 100vh;
  background: url("../../assets/IMG_0167.jpg") no-repeat center center;
  background-color: #aaa;
  background-size: cover;
}

div{
  color: #fff;
  font-family: 'Sawarabi Mincho', sans-serif;
  font-size: 90px;
  user-select: none;
  /* text-shadow: 4px 4px 4px #aaa; */
  spacing: 0.1em;
  line-height: 1.2em;
}

.name{
  color:white;
}

.container-fluid{
  padding-top: 130px;
}

.btn{
  height: 50px;
  font-size: 25px;
  line-height: 1.4em;
  border-radius: 10px;
  border-color: white;
  text-shadow: none;
  margin-top: 100px;
}

.btn:hover{
  background-color: white;
  color: #663333;
  cursor: pointer;
  text-decoration: none;
}

.clicked{
  color: white!important;
  transition: all 600ms 0s ease;
}

.welcome{
  background: white;
  transition: all 600ms 0s ease;
}
</style>
