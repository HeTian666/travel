<template>
  <ul class="list">
    <li class="item"
        v-for="item of letters"
        :key="item"
        :ref="item"
        @click="handleLetterClick"
        @touchstart="handelTouchstart"
        @touchmove="handelTouchMove"
        @touchend="handelTouchEnd"
    >{{ item }}</li>
  </ul>
</template>

<script>
export default {
  name: 'CityAlphabet',
  props: {
    cities: Object
  },
  data () {
    return {
      touchStatus: false,
      startY: 0,
      timers: null
    }
  },
  computed: {
    letters () {
      const letters = []
      for (let i in this.cities) {
        letters.push(i)
      }
      return letters
    }
  },
  updated () {
    this.startY = this.$refs['A'][0].offsetTop
  },
  methods: {
    handleLetterClick (e) {
      this.$emit('change', e.target.innerText)
    },
    handelTouchstart () {
      this.touchStatus = true
    },
    handelTouchMove (e) {
      if (this.touchStatus) {
        if (this.timers) {
          clearTimeout(this.timers)
        }
        this.timers = setTimeout(() => {
          const touchY = e.touches[0].clientY - 79
          const index = Math.floor((touchY - this.startY) / 20)
          if (index >= 0 && index < this.letters.length) {
            this.$emit('change', this.letters[index])
          }
        }, 16)
      }
    },
    handelTouchEnd () {
      this.touchStatus = false
    }
  }
}
</script>

<style lang="stylus" scoped>
@import '~styles/varibles.styl'
  .list
    display: flex
    flex-direction: column
    justify-content: center
    position: absolute
    top:1.54rem
    right: 0
    bottom: 0
    width: 0.4rem
    .item
      text-align: center
      height: 0.4rem
      line-height: 0.4rem
      color: $bgColor
</style>
