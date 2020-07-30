<template>
  <section class="order">
    <HeaderTop :title="headerTitle">
    </HeaderTop>
    <section class="order_no_login">
      <img src="./images/person.png" alt="">
      <h3>登录后查看外面订单</h3>
      <button>立即登录</button>
    </section>
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
      headerTitle: '订单列表'
    }
  }
}
</script>

<style lang="stylus" rel="stylesheet/stylus">
  @import '../../commom/stylus/mixins.styl'
  .order
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
    .order_no_login
      padding-top 140px
      width 60%
      margin 0 auto
      text-align center
      >img
        display block
        width 100%
        height 30%
      >h3
        margin 4px
        padding 10px
        font-size 16px
        color #6a6a6a
      >button
        outline none
        padding 10px 20px
        background #409EFF
        color #ffffff
        border 0
        border-radius 5px
        font-size 16px
</style>
