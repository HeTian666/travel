<template>
    <div class="header">
      <div class="header-left">
        <div class="iconfont return-icon">&#xe624;</div>
      </div>
      <div class="header-input">
        <span class="iconfont">&#xe632;</span>
        输入城市/景点/游玩主题
      </div>
      <div class="header-right">
        城市
        <span class="iconfont down-icon">&#xe6aa;</span>
      </div>
    </div>
</template>

<script>
export default {
  name: 'HomeHeader'
}
</script>

<style lang="stylus" scoped>
@import '~@/assets/varibles.styl'
    .header
      display: flex
      height: 0.86rem
      line-height 0.86rem
      background: $bgColor
      color: #fff
      .header-left
        width: 0.64rem
        float: left
        .return-icon
          text-align: center
          font-size: 0.38rem
      .header-input
        flex: 1
        background: #fff
        height: 0.64rem
        line-height: 0.64rem
        margin-top: 0.12rem
        margin-left: 0.2rem
        padding-left:0.12rem
        border-radius: 0.06rem
        color: #ccc
      .header-right
        width: 1.24rem
        float: right
        text-align: center
        .down-icon
          font-size: 0.24rem
          margin-left: -0.04rem
</style>
