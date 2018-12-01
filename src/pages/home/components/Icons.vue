<template>
  <div class="waper">
    <div class="icon">
      <div class="icon-img">
        <img class="icon-img-content" src="//s.qunarzz.com/vacation_react/freetrip/local.png">
      </div>
      <p class="icon-desc">热门景点</p>
    </div>
  </div>
</template>

<script>
export default {
  name: 'HomeIcons'
}
</script>

<style lang="stylus" scoped>
  @import '~styles/varibles.styl'
  .waper
    overflow: hidden
    width:100%
    height: 0
    padding-bottom: 50%
    .icon
      position: relative
      overflow: hidden
      float: left
      width: 25%;
      height: 0
      padding-bottom: 25%
      .icon-img
        position: absolute
        top: 0
        left: 0
        right: 0
        bottom: 0.44rem
        padding: 0.1rem
        .icon-img-content
          display: block
          margin: 0 auto
          height: 100%
      .icon-desc
        position: absolute
        left: 0
        right: 0
        bottom: 0
        height: 0.44rem
        line-height 0.44rem
        text-align: center
        color: $darkTextColor
</style>
