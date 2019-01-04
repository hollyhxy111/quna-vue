<template>
  <div class="icons">
    <swiper>
      <swiper-slide v-for="(page, index) of pages" :key="index">
        <div class="icon" v-for="item of page" :key="item.id">
          <div class="icon-img">
            <img class="icon-img-content" :src="item.imgUrl">
          </div>
          <p class="icon-desc">{{item.desc}}</p>
        </div>
      </swiper-slide>
    </swiper>
  </div>
</template>

<script>
export default {
  name: 'HomeIcons',
  data () {
    return {
      iconsList: [{
        id: '0001',
        imgUrl: require('@/assets/images/p1.png'),
        desc: '热门景点'
      }, {
        id: '0002',
        imgUrl: require('@/assets/images/p2.png'),
        desc: '一日游'
      }, {
        id: '0003',
        imgUrl: require('@/assets/images/p3.png'),
        desc: '北京必游'
      }, {
        id: '0004',
        imgUrl: require('@/assets/images/p4.png'),
        desc: '帝都范儿'
      }, {
        id: '0005',
        imgUrl: require('@/assets/images/p5.png'),
        desc: '动植物园'
      }, {
        id: '0006',
        imgUrl: require('@/assets/images/p6.png'),
        desc: '故宫'
      }, {
        id: '0007',
        imgUrl: require('@/assets/images/p7.png'),
        desc: '名胜古迹'
      }, {
        id: '0008',
        imgUrl: require('@/assets/images/p8.png'),
        desc: '北京滑雪'
      }, {
        id: '0009',
        imgUrl: require('@/assets/images/p9.png'),
        desc: '给你好看'
      }]
    }
  },
  computed: {
    pages () {
      const pages = []
      this.iconsList.forEach((item, index) => {
        const page = Math.floor(index / 8)
        if (!pages[page]) {
          pages[page] = []
        }
        pages[page].push(item)
      })
      return pages
    }
  }
}
</script>

<style lang="stylus" scoped>
@import '~styles/varibles.styl'
@import '~styles/mixins.styl'
.icons >>> .swiper-container
  height: 0
  padding-bottom: 46%
.icons
  margin-top: .5rem
  .icon
    position: relative
    float: left
    width: 25%
    height: 0
    padding-bottom: 23%
    .icon-img
      position: absolute
      top: 0
      left: 0
      right: 0
      bottom: .88rem
      box-sizing: border-box
      padding: .1rem
      .icon-img-content
        display: block
        margin: 0 auto
        height: 100%
    .icon-desc
      position: absolute
      left: 0
      right: 0
      bottom: 0
      height: .88rem
      line-height: .88rem
      text-align: center
      color: $darkTextColor
      ellipsis()
</style>
