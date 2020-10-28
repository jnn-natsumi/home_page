<template>
  <section class="work">
    <AppBackgroundHolder :title="title"/>
    <h2>作品</h2>
  </section>
</template>
<script>
import AppBackgroundHolder from './AppBackgroundHolder.vue'

export default {
  data () {
    return {
      title: 'Work'
    }
  },
  components: {
    AppBackgroundHolder
  }
}
</script>
