<template>
  <section class="contact">
    <AppBackgroundHolder :title="title"/>
    <div class="section__title2">
            <img src="../assets/img/contact1.jpg" alt="" class="img-fluld rounded-circle">
            <p>thank you for reading</p>
        </div>
    <v-container>
        <v-row class="about__contents">
            <v-col md="5" class="about__contents-text">
              <ul>
                <p>Social Networking Service</p>
                <li><a href="https://github.com/jnn-natsumi" target="_bank"><img src="https://img.icons8.com/fluent/48/000000/github.png" class="icon"></a><br>Github</li>
                <li><a href="https://qiita.com/natsumi_23" target="_bank"><img src="../assets/img/contact.png" class="icon"></a><br>Qiita</li>
                <li><a href="https://twitter.com/home?lang=ja" target="_bank"><img src="../assets/img/contact2.png" class="icon"></a><br>Twitter</li>
              </ul>
            </v-col>
        </v-row>
        <div class="section__title2">
          <div class="section__title2-text">Please give me your impression!!<br><p class="me">感想を聞かせてください。</p></div>
            <p>名前：<input v-model="message" placeholder=" name"></p>
            <p>一言：<input v-model="message" placeholder=" messes"></p>
            <input type="checkbox" id="Excellent" value="Excellent" v-model="checkedNames">
            <label for="Excellent">Excellent</label>
            <input type="checkbox" id="Good" value="Good" v-model="checkedNames">
            <label for="Good">Good</label>
            <input type="checkbox" id="Poor" value="Poor" v-model="checkedNames">
            <label for="Poor">Poor</label>
            <AppButton :button-text="buttonText" :url="url"/>
        </div>
        <div class="margin"></div>
      </v-container>
  </section>
</template>
<script>
import AppBackgroundHolder from './AppBackgroundHolder.vue'
import AppButton from './AppButton.vue'

export default {
  data () {
    return {
      title: 'Contact',
      buttonText: ' send ',
      url: '/'
    }
  },
  components: {
    AppBackgroundHolder,
    AppButton
  }
}
</script>

<style lang="scss" scoped>
.section__title2 {
    padding-top: 20px;
    text-align: center;

    &-text {
      font-family: 'Staatliches', cursive;
      font-weight: 700;
      font-size: 20px;
      color: #ffa500;
    }
  }
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

.bot {
  font-size: 12px;
}

p {
  text-align: center;
  padding-bottom: 5px;
}

.me {
  font-size: 14px;
  text-align: center;
  padding-bottom: 5px;
}

.margin {
  padding-bottom: 50px;
}

input, textarea {
  border: solid #1e366a 1px;
}
</style>
