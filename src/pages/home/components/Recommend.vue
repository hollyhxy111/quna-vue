<template>
  <div>
    <div class="guess-u-like">猜你喜欢</div>
    <ul>
      <li class="item border-bottom" v-for="item of recommendList" :key="item.id">
        <img class="item-img" :src="item.imgUrl">
        <div class="item-info">
          <p class="item-title">{{item.title}}</p>
          <p class="item-desc">{{item.desc}}</p>
          <button class="item-btn">查看详情</button>
        </div>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'HomeRecommend',
  props: {
    recommendList: Array
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
.item
  overflow: hidden
  display: flex
  height: 6rem
  .item-img
    width: 5.4rem
    height: 5.4rem
    padding: .3rem
  .item-info
    flex: 1
    padding: .2rem
    min-width: 0
    .item-title
      line-height: 1.5rem
      font-size: .32rem
      ellipsis()
    .item-desc
      line-height: 1.5rem
      font-size: .28rem
      color: #ccc
      ellipsis()
    .item-btn
      // line-height: 1rem
      margin-top: .7rem
      background: #ff9300
      padding:  .1rem .4rem
      border-radius: .5rem
      color: #fff
</style>
