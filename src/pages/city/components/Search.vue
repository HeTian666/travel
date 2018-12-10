<template>
  <div>
    <div class="search">
      <input class="search-input" type="text" placeholder="输入城市或拼音" v-model="keyword">
    </div>
    <div class="search-content">
      <ul>
        <li class="search-item border-bottom" v-for="item of list" :key="item.id">
          {{ item.name }}
        </li>
      </ul>
    </div>
  </div>
</template>

<script>
export default {
  name: 'CitySearch',
  proos: {
    cities: Object
  },
  data () {
    return {
      keyword: '',
      list: [],
      timer: null
    }
  },
  watch: {
    keyword () {
      if (this.timer) {
        clearTimeout(this.timer)
      }
      if (!this.keyword) {
        this.list = []
        return
      }
      this.timer = setTimeout(() => {
        const result = []
        console.log(this.cities)
        this.list = result
      }, 100)
    }
  }
}
</script>

<style lang="stylus" scoped>
@import '~styles/varibles.styl'
  .search
    height: 0.72rem
    padding: 0 0.1rem
    background: $bgColor
    .search-input
      width: 100%
      height: 0.62rem
      line-height 0.62rem
      text-align: center
      border-radius: 0.06rem
      color: #666
      padding: 0 0.1rem
      box-sizing: border-box
  .search-content
    z-index: 1
    overflow: hidden
    position: absolute
    top: 1.58rem
    left: 0
    right: 0
    bottom: 0
    background: #eee
    .search-item
      line-height: 0.62rem
      padding-left: 0.2rem
      background: #fff
      color: #666
</style>
