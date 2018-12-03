<template>
    <div class="header">
      <div class="header-left">
        <div class="iconfont return-icon">&#xe624;</div>
      </div>
      <div class="header-input">
        <span class="iconfont">&#xe632;</span>
        输入城市/景点/游玩主题
      </div>
      <router-link to='/city'>
        <div class="header-right">
          {{ this.city }}
          <span class="iconfont down-icon">&#xe6aa;</span>
        </div>
      </router-link>
    </div>
</template>

<script>
export default {
  name: 'HomeHeader',
  props: {
    city: String
  }
}
</script>

<style lang="stylus" scoped>
  @import '~styles/varibles.styl'
    .header
      display: flex
      height: $headerHeight
      line-height: $headerHeight
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
        color: #fff
        .down-icon
          font-size: 0.24rem
          margin-left: -0.04rem
</style>
