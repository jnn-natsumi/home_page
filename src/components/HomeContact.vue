<template>
    <sectipn class="home-contact">
        <div class="section__title">
            <div class="section__title-text">04. contact</div>
        </div>
        <v-container fluid fill-height class="home-contact__content">
            <v-row class="home-contact__contents">
            <h5>私が登録しているSNSです。フォローお願いします♩</h5>
            </v-row>
            <v-row class="home-contact__contents">
                <v-col md="5" class="home-contact__contents-img">
                    <img src="../assets/img/work.jpg" alt="" class="img-fluid">
                </v-col>
                <v-col md="5" class="home-contact__contents-text">
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
      buttonText: '>> Contact Me <<',
      url: '/contact'
    }
  },
  components: {
    AppButton
  }
}
</script>

<style lang="scss" scoped>
.home-contact__content {
    background-size: cover;
    background-position: center center;
    width: 100%;
    height:  50vh;
    position: relative;
}
.home-contact__contents {
    margin-top: 20px;
    justify-content: center;

    &-img {
        text-align: center;
    }

    &-text {
        word-wrap: break-word;
    }
}

.home-contact__contents h5 {
    color:   #3cb371;
    text-align: center;
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
        color: #3cb371;
    }
}
</style>
