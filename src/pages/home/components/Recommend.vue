<template>
  <div>
    <div class="title">热销推荐</div>
    <ul>
      <li class="item border-bottom" v-for="list of commendLists" :key="list.id">
        <img class="item-img" :src="list.imgUrl">
        <div class="item-info">
          <p class="item-title">{{ list.title }}</p>
          <p class="item-desc">{{ list.desc }}</p>
          <button class="item-button">查看详情</button>
        </div>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'HomeRecommend',
  data () {
    return {
      commendLists: [
        {
          id: '0001',
          imgUrl: 'https://imgs.qunarzz.com/p/tts4/1412/53/5341eaedd0573f07cdb.jpg_180x120_2deb0840.jpg',
          title: '大连香洲旅游度假区',
          desc: '将壮观诠释到完美，将梦想传递给世界'
        },
        {
          id: '0001',
          imgUrl: 'https://imgs.qunarzz.com/p/tts4/1412/53/5341eaedd0573f07cdb.jpg_180x120_2deb0840.jpg',
          title: '大连香洲旅游度假区',
          desc: '将壮观诠释到完美，将梦想传递给世界'
        },
        {
          id: '0001',
          imgUrl: 'https://imgs.qunarzz.com/p/tts4/1412/53/5341eaedd0573f07cdb.jpg_180x120_2deb0840.jpg',
          title: '大连香洲旅游度假区',
          desc: '将壮观诠释到完美，将梦想传递给世界'
        },
        {
          id: '0001',
          imgUrl: 'https://imgs.qunarzz.com/p/tts4/1412/53/5341eaedd0573f07cdb.jpg_180x120_2deb0840.jpg',
          title: '大连香洲旅游度假区',
          desc: '将壮观诠释到完美，将梦想传递给世界'
        },
        {
          id: '0001',
          imgUrl: 'https://imgs.qunarzz.com/p/tts4/1412/53/5341eaedd0573f07cdb.jpg_180x120_2deb0840.jpg',
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
  .item
    overflow: hidden
    display: flex
    height: 1.9rem
    .item-img
      width: 1.7rem
      height: 1.7rem
      padding: 0.1rem
    .item-info
      flex: 1
      padding: 0.1rem
      min-width: 0
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
      .item-button
        height: 0.44rem;
        line-height: 0.44rem
        margin-top: 0.16rem
        background: #ff9300
        padding: 0 0.2rem
        margin-top: 0.16rem
        border-radius: 0.06rem
        color: #fff
</style>
