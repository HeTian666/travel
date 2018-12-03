<template>
  <div class="list" ref="wrapper">
    <div>
      <div class="area">
        <div class="title border-topbottom">当前城市</div>
        <div class="buttom-list">
          <div class="buttom-wrapper">
            <div class="buttom">北京</div>
          </div>
        </div>
      </div>
      <div class="area">
        <div class="title border-topbottom">热门城市</div>
        <div class="buttom-list">
          <div class="buttom-wrapper">
            <div class="buttom">北京</div>
          </div>
          <div class="buttom-wrapper">
            <div class="buttom">北京</div>
          </div>
          <div class="buttom-wrapper">
            <div class="buttom">北京</div>
          </div>
          <div class="buttom-wrapper">
            <div class="buttom">北京</div>
          </div>
          <div class="buttom-wrapper">
            <div class="buttom">北京</div>
          </div>
        </div>
      </div>
      <div class="area">
        <div class="title border-topbottom">A</div>
        <ul class="item-list">
          <li class="item border-bottom">阿拉善</li>
          <li class="item border-bottom">阿拉善</li>
          <li class="item border-bottom">阿拉善</li>
        </ul>
      </div>
      <div class="area">
        <div class="title border-topbottom">B</div>
        <ul class="item-list">
          <li class="item border-bottom">保定</li>
          <li class="item border-bottom">保定</li>
          <li class="item border-bottom">保定</li>
          <li class="item border-bottom">保定</li>
          <li class="item border-bottom">保定</li>
          <li class="item border-bottom">保定</li>
          <li class="item border-bottom">保定</li>
          <li class="item border-bottom">保定</li>
          <li class="item border-bottom">保定</li>
        </ul>
      </div>
    </div>
  </div>
</template>

<script>
import Bscroll from 'better-scroll'
export default {
  name: 'CityList',
  mounted () {
    this.scroll = new Bscroll(this.$refs.wrapper)
  }
}
</script>

<style lang="stylus" scoped>
@import '~styles/varibles.styl'
.border-topbottom
  &:before
    background: #ccc
  &:after
    background: #ccc
.border-bottom
  &:before
    background: #ccc
.list
  overflow: hidden
  position: absolute
  top: 1.58rem
  left: 0
  bottom: 0
  right: 0
  .title
    height: 0.54rem
    line-height: 0.54rem
    background: #eee
    padding-left: 0.2rem
    color: #666
    font-size: 0.26rem
  .buttom-list
    overflow: hidden
    padding: 0.1rem 0.6rem 0.1rem 0.1rem
    .buttom-wrapper
      float: left
      width: 33.33%
      .buttom
        margin: 0.1rem
        padding: 0.1rem 0
        text-align: center
        border: 0.02rem solid #ccc
        border-radius: 0.06rem
  .item-list
    .item
      height: 0.76rem
      line-height: 0.76rem
      padding-left: 0.2rem
</style>
