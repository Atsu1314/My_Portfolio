<template lang="html">
  <div class="origin container-fuluid" :class="{show : show_main()}" >
    <div v-show="move1" class="btn row w-75" :class="{btn_after : move2}">
      kaigyou <br> kaigyou <br>kaigyou <br>kaigyou <br>kaigyou <br> kaigyou <br>kaigyou <br>kaigyou <br>kaigyou <br>kaigyou <br>
      kaigyou <br> kaigyou <br>kaigyou <br>kaigyou <br>kaigyou <br> kaigyou <br>kaigyou <br>kaigyou <br>kaigyou <br>kaigyou <br>
      kaigyou <br> kaigyou <br>kaigyou <br>kaigyou <br>kaigyou <br> kaigyou <br>kaigyou <br>kaigyou <br>kaigyou <br>kaigyou <br>
      kaigyou <br> kaigyou <br>kaigyou <br>kaigyou <br>kaigyou <br> kaigyou <br>kaigyou <br>kaigyou <br>kaigyou <br>kaigyou <br>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    showMain : {
      type: Boolean,
      default: false
    }
  },
  data() {
    return {
      move1 : false,
      move2 : false,
    }
  },
  methods:{
    move() {
      setTimeout(() => this.move1 = true, 800),
      setTimeout(() => this.move2 = true, 1000)
    },
    show_main() {
      if (this.showMain === true) {
        setTimeout(this.move(),0)
      }
      return this.showMain
    }
  }
}
</script>

<style lang="css" scoped>
div{
  /* font-size: 50px; */
}

.origin{
  height: 100vh;
}

.show{
  height: 100vh;
  background: url("../assets/IMG_0174.jpg") center center;
  background-size: cover;
  background-color:#ffc978;
  opacity: 0.5;
  transition: all 600ms 0ms ease;
}

.btn{
  overflow: scroll;
  width: 0px;
  height: 0px;
  background-color: #ffc978;
  opacity: 0;
}

.btn_after {
  height: 100vh;
  background-color: #eee;
  opacity: 0.9;
  transition: all 1200ms 0ms ease;
}
</style>
