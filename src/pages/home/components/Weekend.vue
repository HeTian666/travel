<template>
  <div>
    <div class="title">周末去哪儿</div>
    <ul>
      <li class="item border-bottom" v-for="list of weekendList" :key="list.id">
        <div class="item-img-content">
          <img class="item-img" :src="list.imgUrl">
        </div>
        <div class="item-info">
          <p class="item-title">{{ list.title }}</p>
          <p class="item-desc">{{ list.desc }}</p>
        </div>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'HomeWeekend',
  props: {
    weekendList: Array
  }
}
</script>

<style lang="stylus" scoped>
@import '~styles/mixins.styl'
  .title
    width: 100%
    height: 0.8rem
    line-height: 0.8rem
    background: #eee
    text-indent: 0.2rem
  .item-img-content
    overflow: hidden
    height: 0
    padding-bottom: 37.09%
    .item-img
      width: 100%
  .item-info
    padding: 0.1rem
    .item-title
      height: 0.54rem
      line-height: 0.54rem
      font-size: .32rem
      ellipsis()
    .item-desc
      height: 0.4rem
      line-height: 0.4rem
      color: #ccc
      ellipsis()
</style>
