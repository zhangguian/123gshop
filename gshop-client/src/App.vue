<template>
  <div id="app">
    <router-view></router-view>
    <!-- <Msite /> -->
    <FooterGuide v-show="$route.meta.showFooter"></FooterGuide>
  </div>
</template>

<script>
// import Msite from './pages/Msite/Msite'
import FooterGuide from './components/FooterGuide/FooerGuide.vue'

export default {
  name: 'App',
  components: {
    FooterGuide
    // Msite
  }
}
</script>

<style lang="stylus" scoped>
  #app
    width 100%
    height 100%
    background #f5f5f5
    position relative
</style>
