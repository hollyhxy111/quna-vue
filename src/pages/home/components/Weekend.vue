<template>
  <div>
    <div class="guess-u-like">周末去哪儿</div>
    <ul>
      <li class="item border-bottom" v-for="item of recommendList" :key="item.id">
        <div class="item-img-wrapper">
          <img class="item-img" :src="item.imgUrl">
        </div>
        <div class="item-info">
          <p class="item-title">{{item.title}}</p>
          <p class="item-desc">{{item.desc}}</p>
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
      recommendList: [{
        id: '0001',
        imgUrl: 'http://img1.qunarzz.com/sight/source/1505/7d/df6ff468331c43.jpg_r_640x214_1f3783d0.jpg',
        title: '上海必打卡',
        desc: '中西合璧，现代和传统各有各的精彩'
      }, {
        id: '0002',
        imgUrl: 'http://img1.qunarzz.com/sight/source/1505/7d/df6ff468331c43.jpg_r_640x214_1f3783d0.jpg',
        title: '上海必打卡',
        desc: '中西合璧，现代和传统各有各的精彩'
      }, {
        id: '0003',
        imgUrl: 'http://img1.qunarzz.com/sight/source/1505/7d/df6ff468331c43.jpg_r_640x214_1f3783d0.jpg',
        title: '上海必打卡',
        desc: '中西合璧，现代和传统各有各的精彩'
      }]
    }
  }
}
</script>

<style lang="stylus" scoped>
@import '~styles/mixins.styl'
.guess-u-like
  margin-top: 1rem
  line-height: 2rem
  background: #eee
  text-indent: .4rem
.item-img-wrapper
  overflow: hidden
  height: 0
  padding-bottom: 33.4%
  .item-img
    width: 100%
.item-info
  padding: .2rem
  margin-bottom: .5rem
  .item-title
    line-height: 1.5rem
    font-size: .32rem
    ellipsis()
  .item-desc
    line-height: 1.5rem
    font-size: .28rem
    color: #ccc
    ellipsis()
</style>
