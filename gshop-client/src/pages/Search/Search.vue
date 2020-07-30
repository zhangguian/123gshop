<template>
  <section class="search">
    <HeaderTop :title="headerTitle">
    </HeaderTop>
    <form class="search_form">
      <input type="search" name="search" class="search_input" placeholder="请输入商家或商品名称" />
      <input type="submit" name="submit" class="search_submit" />
    </form>
  </section>
</template>

<script>
import HeaderTop from '../../components/HeaderTop/headerTop'
export default {
  components: {
    HeaderTop
  },
  data () {
    return {
      headerTitle: '搜索'
    }
  }
}
</script>

<style lang="stylus" rel="stylesheet/stylus">
  @import '../../commom/stylus/mixins.styl'
  .search
    width 100%
    overflow hidden
    .header
      background #409EFF
      position fixed
      z-index 1000
      left 0
      top 0
      width 100%
      height 45px
      .header_search
        position absolute
        left 15px
        top 50%
        transform translateY(-50%)
        width 10%
        height 50%
        .icon-search
          font-size 25px
          color #ffffff
      .header_title
        position absolute
        left 50%
        top 50%
        transform translate(-50%, -50%)
        width 50%
        color #ffffff
        text-align center
        .header_title_text
          font-size 20px
          color #ffffff
          display block
      .header_login
        position absolute
        right 15px
        top 50%
        transform translateY(-50%)
        color #ffffff
    .search_form
      clearFix()
      margin-top 45px
      background-color #fff
      padding 12px 8px
      input
        height 35px
        padding 0 4px
        border-radius 2px
        font-weight bold
        outline none
        &.search_input
          float left
          width 79%
          border 4px solid #f2f2f2
          font-size 14px
          color #333
          background-color #f2f2f2
        &.search_submit
          float right
          width 18%
          border 4px solid #409EFF
          font-size 16px
          color #fff
          background-color #409EFF
</style>
