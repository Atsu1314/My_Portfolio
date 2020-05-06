<template id="">
  <div class="jumbotron junbotron-extend">
    <div class="container-fluid text-center">
      <div class="d-none d-md-block">
        <p :class="{text_opacity : getInOfTop}">Welcome to</p>
        <p :class="{text_opacity : getInOfTop}">Muta Atsuyoshi's</p>
        <p :class="{text_opacity : getInOfTop}">Portfolio.</p>
      </div>
      <div class="d-md-none smart">
        <p :class="{text_opacity : getInOfTop}">Welcome to</p>
        <p :class="{text_opacity : getInOfTop}">Muta Atsuyoshi's</p>
        <p :class="{text_opacity : getInOfTop}">Portfolio.</p>
      </div>
    </div>
    <div class="btn" @click="welcome()" :class="{clicked : getInOfTop}"><p>Get in</p></div>

  </div>
</template>

<script type="text/javascript">
  export default {
    data(){
      return{
        getInOfTop: false
      }
    },
    methods: {
      welcome() {
        this.getInOfTop = true,
        this.$emit('getIn')
      }
    }
  }
</script>

<style media="screen" scoped>
@import url('https://fonts.googleapis.com/css?family=Sawarabi+Mincho');
.junbotron-extend{
  position:relative;
  height: 100vh;
  min-height: 600px;
  background: url("../assets/IMG_0174.jpg") no-repeat center center;
  background-color: #aaa;
  background-size: cover;
  margin-bottom: 0;
  border-radius: 5px 5px 0 0;
}

div{
  color: #fff;
  font-family: 'Sawarabi Mincho', sans-serif;
  font-size: 90px;
  user-select: none;
  spacing: 0.1em;
  line-height: 1.2em;
}

.text_opacity{
  color: #ffc978;
  opacity: 0;
  transition: all 400ms 0ms ease;
}

.smart{
  font-size: 45px;
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
  margin-top: 50px;
}

.btn:hover{
  background-color: white;
  color: #663333;
  cursor: pointer;
  text-decoration: none;
}

.clicked{
  color: #ffc978!important;
  opacity: 0;
  transition: all 400ms 0s ease;
}
</style>
