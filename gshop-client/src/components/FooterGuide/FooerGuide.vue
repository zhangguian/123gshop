<template>
    <div class="footer_guide">
      <a href="javascript:;" class="guide_item" :class="{on: '/msite' === $route.path}" @click="goTo('/msite')">
        <span class="item_icon">
          <i class="iconfont icon-attract"></i>
        </span>
        <span class="span">外卖</span>
      </a>
      <a href="javascript:;" class="guide_item" :class="{on: '/search' === $route.path}" @click="goTo('/search')">
        <span class="item_icon">
          <i class="iconfont icon-sousuo"></i>
        </span>
        <span class="span">搜索</span>
      </a>
      <a href="javascript:;" class="guide_item" :class="{on: '/order' === $route.path}" @click="goTo('/order')">
        <span class="item_icon">
          <i class="iconfont icon-logooo_huabanfuben"></i>
        </span>
        <span class="span">订单</span>
      </a>
      <a href="javascript:;" class="guide_item" :class="{on: '/profile' === $route.path}" @click="goTo('/profile')">
        <span class="item_icon">
          <i class="iconfont icon-gerenzhongxinwoderenwubiaozhuntoumianxing"></i>
        </span>
        <span class="span">我的</span>
      </a>
    </div>
</template>

<script>
export default {
  methods: {
    goTo (path) {
      this.$router.replace(path)
    }
  }
}
</script>

<style lang="stylus" rel="stylesheet/stylus">
  @import '../../commom/stylus/mixins.styl'
  .footer_guide
    top-border-1px(#e4e4e4)
    position fixed
    z-index 1000
    left 0
    bottom 0
    background #ffffff
    width 100%
    height 50px
    display flex
    .guide_item
      display flex
      flex 1
      text-align center
      flex-direction column
      align-items center
      justify-content center
      margin 5px
      color #999999
      &.on
        color #409EFF
      .span
        margin-top 3px
      span
      font-size 12px
      margin-top 2px
      margin-bottom 2px
      .iconfont
        font-size 22px
</style>
