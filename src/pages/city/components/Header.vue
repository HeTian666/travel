<template>
  <div class="header">
    城市选择
    <router-link to="/">
      <div class="iconfont city-return">&#xe624;</div>
    </router-link>
  </div>
</template>

<script>
export default {
  name: 'CityHeader'
}
</script>

<style lang="stylus" scoped>
@import '~styles/varibles.styl'
  .header
    position: relative
    overflow: hidden
    height: $headerHeight
    line-height $headerHeight
    text-align: center
    color: #ffffff
    background: $bgColor
    .city-return
      position: absolute
      width: 0.64rem
      top: 0
      left: 0
      color: #fff
</style>
