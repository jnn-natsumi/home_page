<template>
  <section class="blog">
    <AppBackgroundHolder :title="title"/>
    <h2>作品</h2>
  </section>
</template>
<script>
import AppBackgroundHolder from './AppBackgroundHolder.vue'

export default {
  data () {
    return {
      title: 'Blog'
    }
  },
  components: {
    AppBackgroundHolder
  }
}
</script>
