<template>
    <sectipn class="home-work">
        <div class="section__title">
            <div class="section__title-text">02. Work</div>
        </div>
        <v-container>
            <v-row class="home-work__contents">
                <v-col md="5" class="home-work__contents-img">
                    <img src="../assets/img/work.jpg" alt="" class="img-fluid">
                </v-col>
                <v-col md="5" class="home-work__contents-text">
                    <p>コンニチワ</p>
                    <p>natumiと申します。</p>
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
      buttonText: '詳しく見る',
      url: '/work'
    }
  },
  components: {
    AppButton
  }
}
</script>

<style lang="scss" scoped>
.home-work__contents {
    margin-top: 20px;
    justify-content: center;
    border: 3px solid #1e90ff;

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

.home-work::before {
  content:"";
  position: absolute;
  bottom: 0;
  left: 0;
  width: 0;
  height: 0;
  border-style: solid;
  /*ここで三角形のサイズを決める。
  必ず幅100vwにして、ブラウザサイズいっぱいにしてください。*/
  border-width: 0 0 100px 100vw ;
  border-color: transparent transparent #fff transparent;
}
</style>
