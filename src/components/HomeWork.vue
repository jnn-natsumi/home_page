<template>
    <sectipn class="home-work">
        <div class="section__title">
            <div class="section__title-text">02. Work</div>
        </div>
        <v-container fluid fill-height class="home-work__content">
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
  border-width: 0 0 300px 100vw ;
  border-color: transparent transparent #ffe4c4 transparent;
}
</style>
