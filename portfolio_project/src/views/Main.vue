<template lang="html">
  <div class="origin container-fuluid" :class="{show : show_main()}" >
    <div v-show="move1" class="btn row w-75" :class="{btn_after : move2}">
      <div class="row">
        <b class="h1 history col-12">H I S T O R Y</b>
        <div class="w-100 row">
          <div class="col-4 p-0">2014/04</div>
          <div class="col-8 p-0">千葉大学 理学部生物学科 入学</div>
        </div>
        <div class="w-100 row">
          <div class="col-4 p-0">2015/04</div>
          <div class="col-8 p-0">千葉大学 数学・情報数理学科 転学科</div>
        </div>
        <div class="w-100 row">
          <div class="col-4 p-0">2018/04</div>
          <div class="col-8 p-0">東京工業大学 情報理工学院 数理・計算科学系 数理計算科学コース 入学</div>
        </div>
        <div class="w-100 row">
          <div class="col-4 p-0">2020/02</div>
          <div class="col-8 p-0">イグニションポイント株式会社 インターンとしてフロントエンド開発を経験</div>
        </div>
        <div class="w-100 row">
          <div class="col-4 p-0">2020/09</div>
          <div class="col-8 p-0">東京工業大学 情報理工学院 数理・計算科学系 数理計算科学コース 修了予定</div>
        </div>
        <!-- <p class="col">2014/04 千葉大学 理学部生物学科 入学</p>
        <p class="col-12">2015/04 千葉大学 数学・情報数理学科 転学科</p>
        <p class="col-12">2018/04 東京工業大学 情報理工学院 数理・計算科学系 数理計算科学コース 入学</p>
        <p class="col-12">2020/02 イグニションポイント株式会社 インターンとしてフロントエンド開発を経験</p> -->
      </div>

      <div class="row">
        <b class="h1 col-12 works">W O R K S</b>
        <div class="w-100 row">
          <div class="col-4 p-0">2020/08</div>
          <div class="col-8 p-0">習作としてJavaScriptのフレームワークVue.jsを用いて<a href="" class="href">本ポートフォリオサイト</a>を自作．ソースコードはGitHub上で公開しています．</div>
        </div>
      </div>
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

.history{
  padding-bottom: 30px;
}

.works{
  padding-top: 30px;
}

.href{
  color:red;
}
</style>
