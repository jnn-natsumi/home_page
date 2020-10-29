<template>
    <sectipn class="home-work">
        <div class="section__title">
            <div class="section__title-text">02. Work</div>
        </div>
        <v-container fluid fill-height class="home-work__content">
            <v-row class="home-work__contents">
            <h5>イチバン力を入れたアプリの紹介です。他の作品は、MORE "WORK" VIEWから。</h5>
            </v-row>
            <v-row class="home-work__contents">
                <v-col md="3" class="home-work__contents-img">
                    <img src="../assets/img/work.jpg" alt="" class="img-fluid">
                </v-col>
                <v-col md="4" class="home-work__contents-text">
                    <p>ユーザー投稿型の旅行アプリ "APERE" （アペレ）です。<br>
                       ２箇所指定すると中間地点の住所を表示してくれます。<br></p>
                    <p>ターゲットユーザは、遠距離カップルを想定しています！</p>
                    <p>使用言語/フレームワークは、<br>Ruby/Ruby on Rails/HTML&CSS/JavaScriptなどです。<br>
                       制作期間は約２ヶ月間で、RSpecの導入にてこずりました。</p>
                    <p>WORKページから実際にアプリを使ってみてください！</p>
                </v-col>
            </v-row>
            <AppButton :button-text="buttonText" :url="url"/>
        </v-container>
    </sectipn>
</template>

<script>
import AppButton from './AppButton.vue'

export default {
  data () {
    return {
      buttonText: 'more "work" view',
      url: '/work'
    }
  },
  components: {
    AppButton
  }
}
</script>

<style lang="scss" scoped>
.home-work__content {
    background-size: cover;
    background-position: center center;
    width: 100%;
    height:  50vh;
    position: relative;
}
.home-work__contents {
    margin-top: 20px;
    justify-content: center;

    &-img {
        text-align: center;
    }

    &-text {
        word-wrap: break-word;
    }
}

.home-work__contents h5 {
    color:  #1e90ff;
    text-align: center;
}

.home-work__contents p {
    font-family: 'Kosugi Maru', sans-serif;
    font-size: 15px;
}

img {
    width: 200px !important;
    height: 200px !important;
}

.section__title {
    padding-top: 120px;
    text-align: center;

    &-text {
        font-family: 'Londrina Outline', cursive;
        font-weight: 700;
        font-size: 40px;
        color: #1e90ff;
    }
}

.home-work__content::before {
  content:"";
  position: absolute;
  bottom: 0;
  left: 0;
  width: 0;
  height: 0;
  border-style: solid;
  /*ここで三角形のサイズを決める。
  必ず幅100vwにして、ブラウザサイズいっぱいにしてください。*/
  border-width: 0 0 150px 100vw ;
  border-color: transparent transparent #66cdaa transparent;
}
</style>
