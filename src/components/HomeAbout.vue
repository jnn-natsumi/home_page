<template>
    <sectipn class="home-about">
        <div class="section__title">
            <div class="section__title-text">01. About Me</div>
        </div>
        <v-container>
            <v-row class="home-about__contents">
            <h5>私の簡単な自己紹介です。詳細は、MORE "ABOUT" READから。</h5>
            </v-row>
            <v-row class="home-about__contents">
                <v-col md="4" class="home-about__contents-text">
                    <p>こんにちは。natsumiと申します。</p>
                    <p>エンジニアになりたく、<br>前職を退職して転職活動中です(2020/11)。</p>
                    <p>最近は、羽生さんや藤井さんに感動して、<br>将棋を勉強中です。<br>
                       趣味と言えるレベルまで上達したい。</p>
                </v-col>
                <v-col md="3" class="home-about__contents-img">
                    <img src="../assets/img/myphoto.jpg" alt="" class="img-fluid rounded-circle">
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
      buttonText: 'more "about" read',
      url: '/about'
    }
  },
  components: {
    AppButton
  }
}
</script>

<style lang="scss" scoped>
.home-about__contents {
    margin-top: 20px;
    justify-content: center;

    &-img {
        text-align: center;
    }

    &-text {
        word-wrap: break-word;
    }
}
.home-about__contents h5 {
    color: #e65f78;
    text-align: center;
}

.home-about__contents p {
    font-family: 'Kosugi Maru', sans-serif;
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
        color: #e65f78;
    }
}
</style>
