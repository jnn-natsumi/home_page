<template>
  <section class="work">
    <AppBackgroundHolder :title="title"/>
    <v-container>
      <v-row class="work__contents">
        <v-col md="6" class="work__contents-text">
          <a href="http://apere.work/" target="_bank"><img  src="../assets/img/work.jpg" alt="" class="img-fluid"></a>
          <a href="http://apere.work/" target="_bank"><img  src="../assets/img/apere.png" alt="" class="img-fluid"></a>
          <ul>
                <p><a href="http://apere.work/" target="_bank">APERE</a></p>
                <li>概要 ： ユーザー投稿型の旅行アプリ "APERE" （アペレ）です。<br>２箇所指定していただくと中間地点の住所を表示してくれます。</li>
                <li>背景 ： 物理的距離の遠さという２人の"障害"を、少しでも減らせればと思い、このアプリを考えました。</li>
                <li>機能 ： ログイン機能・いいね機能・コメント機能・タグ検索機能</li>
              </ul>
        </v-col>
        <v-col md="6" class="work__contents-text">
          <a href="https://thawing-thicket-84246.herokuapp.com/post/list" target="_bank"><img  src="../assets/img/record1.png" alt="" class="img-fluid"></a>
          <a href="https://thawing-thicket-84246.herokuapp.com/post/list" target="_bank"><img  src="../assets/img/record2.png" alt="" class="img-fluid"></a>
          <ul>
                <p><a href="https://thawing-thicket-84246.herokuapp.com/post/list" target="_bank">Record App</a></p>
                <li>概要 ： ユーザ投稿型の記録アプリ”Record”（レコード）です。プログラミングで課題が解決できたら記録に残して、備忘録に使えます。</li>
                <li>背景 ： Qiitaよりも手軽にメモのように記録が残せるアプリが欲しいと思い、作成しました。</li>
                <li>機能 ： 投稿機能・閲覧機能・削除機能</li>
              </ul>
        </v-col>
      </v-row>
    </v-container>
    <v-container>
      <v-row class="work__contents">
        <v-col md="6" class="work__contents-text">
          <img src="../assets/img/goto1.png" alt="" class="img-fluid">
          <img src="../assets/img/goto2.png" alt="" class="img-fluid">
          <ul>
                <p>GoTo App</p>
                <li>概要 ： 行きたいところをリストアップして記録するアプリを作成しました。デプロイはしてないので、詳細は<a href="https://github.com/jnn-natsumi/GoTo_app">Github</a>へ。</li>
                <li>背景 ： コロナ禍で旅行に行きたい欲が募るばかり・・・。１度リストアップして来たる日に備えることができればなと考え、作成しました。</li>
                <li>機能 ： 投稿機能・削除機能・編集機能</li>
              </ul>
        </v-col>
        <v-col md="6" class="work__contents-text">
          <img src="../assets/img/filmeet1.png" alt="" class="img-fluid">
          <img src="../assets/img/filmeet2.png" alt="" class="img-fluid">
          <ul>
                <p>FilMeet</p>
                <li>現在作成中のアプリです！</li>
                <li>概要 ： 映画館を通して、人と出会えるマッチングアプリです。見たい映画が同じ人を誘って、映画を見に行けます。</li>
                <li>背景 ： 1人で映画を見るのは抵抗ないけど、感動は誰かと共有したい！そんな思いをマッチングアプリにして、実現しようと考え作成してます。</li>
              </ul>
        </v-col>
      </v-row>
      <p>画像をクリックしてもリンク先へ移動できます！</p>
      <div class="margin"></div>
    </v-container>
  </section>
</template>
<script>
import AppBackgroundHolder from './AppBackgroundHolder.vue'

export default {
  data () {
    return {
      title: 'Work'
    }
  },
  components: {
    AppBackgroundHolder
  }
}
</script>

<style lang="scss" scoped>
.work__contents {
    margin-top: 20px;
    justify-content: center;

    &-img {
        text-align: center;
    }

    &-text {
        word-wrap: break-word;
    }
}

img {
    width: 200px !important;
    height: 200px !important;
    transition-property: opacity;
    transition-duration: 1s;
    transition-timing-function: ease;
    transition-delay: 0s;
}

img:hover {
    opacity: 0.5;
}

ul {
  list-style-type: none;
  color: #1e366a;
  border-top: solid #1e366a 3px;/*上のボーダー*/
  border-bottom: solid #1e366a 3px;/*下のボーダー*/
  padding: 0.5em 0 0.5em 1.5em;
}

ul li {
  line-height: 1.5;
  padding: 0.5em 0;
}

.bot {
  font-size: 12px;
}

p {
  text-align: center;
  padding-bottom: 10px;
}

.margin {
  padding-bottom: 20px;
}
</style>
