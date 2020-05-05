<template id="">
  <div class="jumbotron junbotron-extend">
    <div class="container-fluid text-center">
      Wlcome to <p class="name">Muta Atsuyoshi's</p> Portfolio!
    </div>
    <div class="btn"><p>Get in</p></div>
  </div>
</template>

<script type="text/javascript">
  export default {

  }
</script>

<style media="screen" scoped>
@import url('https://fonts.googleapis.com/css?family=Sawarabi+Mincho');
.junbotron-extend{
  position:relative;
  height: 100vh;
  background: url("../../assets/IMG_0167.jpg") no-repeat center center;
  background-size: cover;
}

div{
  color: #fff;
  font-family: 'Sawarabi Mincho', sans-serif;
  font-size: 90px;
  user-select: none;
  text-shadow: 4px 4px 4px #aaa;
  spacing: 0.1em;
  line-height: 1.2em;
}

.name{
  color:#FFF5EE;
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
}

.btn:hover{
  background-color: white;
  color: #663333;
  cursor: pointer;
  text-decoration: none;
}

</style>
