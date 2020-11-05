<template>
    <sectipn class="home-contact">
        <div class="section__title">
            <div class="section__title-text">04. contact</div>
        </div>
        <v-container fluid fill-height class="home-contact__content">
            <v-row class="home-contact__contents">
            <h5>私が登録しているSNSです。</h5>
            </v-row>
            <v-row class="home-contact__contents">
              <ul>
                <p>Social Networking Service</p>
                <li><a href="https://github.com/jnn-natsumi" target="_bank"><img src="https://img.icons8.com/fluent/48/000000/github.png" class="icon"></a><br>Github</li>
                <li><a href="https://qiita.com/natsumi_23" target="_bank"><img src="../assets/img/contact.png" class="icon"></a><br>Qiita</li>
                <li><a href="https://twitter.com/home?lang=ja" target="_bank"><img src="../assets/img/contact2.png" class="icon"></a><br>Twitter</li>
              </ul>
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
    color:   #ffa500;
    text-align: center;
}

img {
    width: 200px !important;
    height: 200px !important;
}

.icon {
    width: 200px !important;
    height: 200px !important;
    transition-property: opacity;
    transition-duration: 1s;
    transition-timing-function: ease;
    transition-delay: 0s;
}

.icon:hover {
    opacity: 0.5;
}

.icon {
    width: 50px !important;
    height: 50px !important;
}

ul {
  text-align: center;
  font-weight: bold;
  list-style-type: none;
  color: #1e366a;
  padding: 0.5em 0 0.5em 1.5em;
  overflow: hidden;
}

ul li {
  line-height: 1.5;
  padding: 0.5em 0;
  float: left;
  width: 140px;
  text-align: center;
}

.section__title {
    padding-top: 120px;
    text-align: center;

    &-text {
        font-family: 'Londrina Outline', cursive;
        font-weight: 700;
        font-size: 40px;
        color: #ffa500;
    }
}
</style>
