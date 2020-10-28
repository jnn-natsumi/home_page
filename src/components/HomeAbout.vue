<template>
    <sectipn class="home-about">
        <div class="section__title">
            <div class="section__title-text">01. About Me</div>
        </div>
        <v-container>
            <v-row class="home-about__contents">
                <v-col md="5" class="home-about__contents-img">
                    <img src="../assets/img/myphoto.jpg" alt="" class="img-fluid rounded-circle">
                </v-col>
                <v-col md="5" class="home-about__contents-text">
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
      buttonText: '>>More Read<<',
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
    border: 3px solid #e65f78;

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
        color: #e65f78;
    }
}
</style>
