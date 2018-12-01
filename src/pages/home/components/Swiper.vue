<template>
  <div class="warp">
    <swiper :options="swiperOption">
      <swiper-slide v-for="item of swiperList" :key="item.id">
        <img class="swiper-img" :src="item.imgUrl">
      </swiper-slide>
      <div class="swiper-pagination"  slot="pagination"></div>
    </swiper>
  </div>
</template>

<script>
export default {
  name: 'HomeSwiper',
  data () {
    return {
      swiperOption: {
        pagination: '.swiper-pagination',
        autoplay: 2000,
        speed: 1000,
        loop: true
      },
      swiperList: [
        {
          id: '0001',
          imgUrl: 'http://img1.qunarzz.com/piao/fusion/1811/c7/9e447c013b556902.jpg_890x330_c74c8ce5.jpg'
        },
        {
          id: '0002',
          imgUrl: 'http://img1.qunarzz.com/piao/fusion/1811/d8/2977624617721802.jpg_890x330_39ab9791.jpg'
        }
      ]
    }
  }
}
</script>

<style lang="stylus" scoped>
  .warp >>> .swiper-pagination-bullet-active
    background: #fff
  .warp
    overflow: hidden
    width: 100%
    height: 0
    background: #333
    padding-bottom: 37.07%
    .swiper-img
      width: 100%
</style>
