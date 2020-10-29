<template>
    <sectipn class="home-blog">
        <div class="section__title">
            <div class="section__title-text">03. blog</div>
        </div>
        <v-container fluid fill-height class="home-blog__content">
            <v-row class="home-blog__contents">
            <h5>よく見ていただいてる３つの記事です。MORE "BLOG" READより、Qiitaなどのブログも紹介しています。</h5>
            </v-row>
            <v-row class="home-blog__contents">
                <v-col md="4" class="home-blog__contents-img">
                    <h4><a href="https://note.com/apart713/n/n07bd0553bc2b" target="_self">悩む行為で自分の人生を踏みとどまってる自分への鼓舞録。</a></h4>
                    <img src="../assets/img/blog1.png" alt="" class="img-fluid">
                </v-col>
                <v-col md="4" class="home-blog__contents-img">
                    <h4><a href="https://note.com/apart713/n/n9a43ca41294d" target="_self">人生の帰路（1）偏差値40から偏差値60の大学へ編入した話。</a></h4>
                    <img src="../assets/img/blog2.png" alt="" class="img-fluid">
                </v-col>
                <v-col md="4" class="home-blog__contents-img">
                    <h4><a href="https://note.com/apart713/n/n409aaad912c7" target="_self">なぜ、完璧主義は悪とされるのか。</a></h4>
                    <img src="../assets/img/blog3.png" alt="" class="img-fluid">
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
      buttonText: 'more "blog" read',
      url: '/blog'
    }
  },
  components: {
    AppButton
  }
}
</script>

<style lang="scss" scoped>
.home-blog__content {
    background-color: #66cdaa;
    background-size: cover;
    background-position: center center;
    width: 100%;
    height:  50vh;
    position: relative;
}

.home-blog__content h5 {
    color: #ffffff;
    text-align: center;
}

.home-blog__contents {
    margin-top: 20px;
    justify-content: center;

    &-img {
        text-align: center;
        z-index: 1;
    }

    &-text {
        word-wrap: break-word;
    }
}
.section__title {
    background-color:#66cdaa;
    padding-top: 120px;
    text-align: center;

    &-text {
        font-family: 'Londrina Outline', cursive;
        font-weight: 700;
        font-size: 40px;
        color:#ffffff;
    }
}
.home-blog__content::before {
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
  border-color: transparent transparent white transparent;
}
</style>
