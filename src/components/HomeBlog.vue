<template>
    <sectipn class="home-blog">
        <div class="section__title">
            <div class="section__title-text">03. blog</div>
        </div>
        <v-container fluid fill-height class="home-blog__content">
            <v-row class="home-blog__contents">
            <h5>Qiitaで投稿した記事です。<br>
                Blog詳細画面は作成中です！しばしお待ちください。</h5>
            </v-row>
            <v-row class="home-blog__contents">
                <v-col md="4" class="home-blog__contents-img">
                    <h5><a href="https://qiita.com/natsumi_23/items/531c53e474a521923a9e" target="_bank">Ruby / RailsでWEBアプリを作成する -- ⑴要件定義、基本設計、詳細設計</a></h5>
                    <img src="../assets/img/blog1.jpg" alt="" class="img-fluid">
                </v-col>
                <v-col md="4" class="home-blog__contents-img">
                    <h5><a href="https://qiita.com/natsumi_23/items/1443b79717ccecda0629" target="_bank">エラーが発生し、MySQLにログインできないためアンインストールを行う</a></h5>
                    <img src="../assets/img/blog2.jpg" alt="" class="img-fluid">
                </v-col>
                <v-col md="4" class="home-blog__contents-img">
                    <h5><a href="https://qiita.com/natsumi_23/items/ee4ad6b0d39e18f548fe" target="_bank">Vue cliで作ったホームページをHerokuでデプロイする </a></h5>
                    <img src="../assets/img/blog3.jpg" alt="" class="img-fluid">
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
      buttonText: 'comming soon!',
      url: '/'
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

img {
    width: 300px !important;
    height: 150px !important;
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
