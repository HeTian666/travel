<template>
  <div>
    <div class="title">周末去哪儿</div>
    <ul>
      <li class="item border-bottom" v-for="list of commendLists" :key="list.id">
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
  data () {
    return {
      commendLists: [
        {
          id: '0001',
          imgUrl: 'http://img1.qunarzz.com/sight/source/1510/6e/1ea71e2f04e.jpg_r_640x214_aa6f091d.jpg',
          title: '大连香洲旅游度假区',
          desc: '将壮观诠释到完美，将梦想传递给世界'
        },
        {
          id: '0002',
          imgUrl: 'http://img1.qunarzz.com/sight/source/1510/6e/1ea71e2f04e.jpg_r_640x214_aa6f091d.jpg',
          title: '大连香洲旅游度假区',
          desc: '将壮观诠释到完美，将梦想传递给世界'
        },
        {
          id: '0003',
          imgUrl: 'http://img1.qunarzz.com/sight/source/1510/6e/1ea71e2f04e.jpg_r_640x214_aa6f091d.jpg',
          title: '大连香洲旅游度假区',
          desc: '将壮观诠释到完美，将梦想传递给世界'
        }
      ]
    }
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
    margin-top: 0.2rem
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
