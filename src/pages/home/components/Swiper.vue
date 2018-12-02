<template>
  <div class="warp">
    <swiper :options="swiperOption" v-if="showSwiper">
      <swiper-slide v-for="item of this.swiperList" :key="item.id">
        <img class="swiper-img" :src="item.imgUrl">
      </swiper-slide>
      <div class="swiper-pagination"  slot="pagination"></div>
    </swiper>
  </div>
</template>

<script>
export default {
  name: 'HomeSwiper',
  props: {
    swiperList: Array
  },
  data () {
    return {
      swiperOption: {
        pagination: '.swiper-pagination',
        autoplay: 2000,
        speed: 1000,
        loop: true
      }
    }
  },
  computed: {
    showSwiper () {
      return this.swiperList.length
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
    padding-bottom: 31%
    .swiper-img
      width: 100%
</style>
