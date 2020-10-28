// トップページのベースとなるコンポーネントであるため、トップページの子コンポーネントはすべてこちらで読み込みます。

<template>
    <section class="home">
        <HomeHero/>
        <HomeAbout/>
        <HomeWork/>
        <HomeBlog/>
    </section>
</template>

<script>
import HomeHero from './HomeHero.vue'
import HomeAbout from './HomeAbout.vue'
import HomeWork from './HomeWork.vue'
import HomeBlog from './HomeBlog.vue'

export default {
  components: {
    HomeHero,
    HomeAbout,
    HomeWork,
    HomeBlog
  }
}
</script>

<style lang="scss" scoped>
.home {
    padding-bottom: 50px
}
</style>
