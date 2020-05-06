<template lang="html">
  <div class="origin" :class="{show : show_main(), move2: move2}" >
    <div v-show="move2" class="btn container" :class="{btn_after : move3}"></div>
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
      move3 : false,
    }
  },
  methods:{
    move() {
      setTimeout(() => this.move1 = true, 700),
      setTimeout(() => this.move2 = true, 1000),
      setTimeout(() => this.move3 = true, 1200)
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
.show{
  height: 860px;
  transition: all 600ms 0ms ease;
}

.btn{
  width: 0px;
  height: 0px;
  background-color: #ffc978;
  opacity: 0;
  /* transition: all 700ms 0ms ease; */
}

.btn_after {
  width: 1200px;
  height: 860px;
  background-color: #eee;
  opacity: 1;
  transition: all 2000ms 0ms ease;
}

.move1{
  background-color:#ffc99b;
  transition: all 700ms 0ms ease;
}

.move2{
  background-color:#ffc978;
  transition: all 700ms 0ms ease;
}
</style>
