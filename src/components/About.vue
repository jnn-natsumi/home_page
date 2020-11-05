<template>
    <section class="about">
        <AppBackgroundHolder :title="title"/>
        <v-container>
          <v-row class="about__contents">
            <v-col md="3" class="about__contents-text">
              <img src="../assets/img/me1.jpg" alt="" class="img-fluld rounded-circle">
              <p>レストランの前にて 2018年</p>
            </v-col>
            <v-col md="5" class="about__contents-text">
              <ul>
                <p>基本情報</p>
                <li>名前 ： natsumi</li>
                <li>所在 ： Tokyo </li>
                <li>言語 ： Ruby / Ruby on Rails / HTML&CSS / JavaScript </li>
              </ul>
              <ul>
                <p>外見について</p>
                <li>身長 ： 163cm</li>
                <li>体型 ： normal </li>
                <li>髪色 ： 黒髪</li>
              </ul>
            </v-col>
          </v-row>

          <v-row class="about__contents">
            <v-col md="5" class="about__contents-text">
              <ul>
                <p>趣味</p>
                <li>映画 ： ショーシャンクの空に</li>
                <li>娯楽 ： 将棋</li>
                <li>旅行 ： 台湾とベトナムは住みたい国 </li>
              </ul>
              <ul>
                <p>一言</p>
                <li class="bot">最近の興味があることは、差別・戦争・歴史です。<br>
                差別・戦争は映画で見漁ってます。<br>
                いつか素敵な社会になるために、自分ができることをしようかなと考えています。
                宇宙に関しては、知ろうとチャレンジして挫折の繰り返し。だけど惹かれます。<br></li>
              </ul>
            </v-col>
            <v-col md="3" class="about__contents-text">
              <img src="../assets/img/me2.jpg" alt="" class="img-fluld rounded-circle">
              <p>証明写真の時 2019年</p>
            </v-col>
          </v-row>
          <p>写真は全て『<a href="https://ai-art.tokyo/">AI画伯</a>』に書いてもらいました。</p>
        </v-container>
    </section>
</template>

<script>
import AppBackgroundHolder from './AppBackgroundHolder.vue'

export default {
  data () {
    return {
      title: 'About'
    }
  },
  components: {
    AppBackgroundHolder
  }
}
</script>

<style lang="scss" scoped>
.about__contents {
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
}

ul {
  list-style-type: none;
  color: #1e366a;
  border-top: solid #1e366a 1px;/*上のボーダー*/
  border-bottom: solid #1e366a 1px;/*下のボーダー*/
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
  padding-bottom: 5px;
}
</style>
